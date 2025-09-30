---
description: Test coverage check for uncommitted and unpushed git changes
allowed-tools: Read, Glob, Grep, Bash, TodoWrite
---

Perform targeted test coverage analysis for files changed in git (uncommitted + unpushed):

## Phase 1: Detect Git Changes

Run git commands to find changed files:

```bash
# Get uncommitted changes (modified, new, staged)
git status --porcelain

# Get unpushed changes (committed but not pushed to main/origin)
git diff main --name-only
git diff origin/main --name-only 2>/dev/null || echo "No remote tracking"
```

Combine results to get full list of changed files since last push.

Filter for source files only:
- Include: `src/**/*.tsx`, `src/**/*.ts` (excluding `.test.` and `.spec.` files)
- Focus on: Components (`src/components/`) and Pages (`src/pages/`)
- Exclude: Test files, config files, docs

## Phase 2: Analyze Each Changed File

For EACH changed source file:

1. **Determine file type**:
   - Component (in `src/components/`)
   - Page (in `src/pages/`)
   - Hook (in `src/hooks/`)
   - Utility (in `src/lib/` or `src/utils/`)

2. **Check for corresponding tests**:
   - Unit test: Same directory with `.test.tsx` or `.test.ts` extension
   - E2E test: Look in `tests/e2e/` for related spec files
   - Use Grep to search test files for references to the component name

3. **Assess test status**:
   - ✅ **HAS TESTS**: Test file exists and imports/references the changed file
   - ⚠️ **TESTS MAY BE OUTDATED**: Test exists but may not cover recent changes
   - ❌ **MISSING TESTS**: No test file found

## Phase 3: Generate Focused Report

Present findings in a pre-commit checklist format:

### 🔍 Changed Files Analysis

List each changed file with test status:

```
src/components/Example/NewComponent.tsx
  Status: ❌ MISSING TESTS
  Type: Component
  Recommendation: Create src/components/Example/NewComponent.test.tsx
  Priority: HIGH (new user-facing component)

src/pages/Startups.tsx
  Status: ⚠️ TESTS MAY BE OUTDATED
  Existing Test: tests/e2e/hero-section-comprehensive.spec.ts
  Recommendation: Review E2E test to ensure new changes are covered
  Priority: MEDIUM

src/lib/utils.ts
  Status: ✅ HAS TESTS
  Existing Test: src/lib/utils.test.ts
  Recommendation: None - covered
```

### 📊 Summary

- Total changed files: X
- Files with tests: X (X%)
- Files without tests: X
- Outdated tests: X

### 🎯 Pre-Commit Checklist

Before committing/pushing, consider:

- [ ] File 1: Create missing test
- [ ] File 2: Update existing test
- [ ] File 3: Add E2E coverage

### 💡 Quick Test Suggestions

For each missing test, provide starter template:

```typescript
// src/components/Example/NewComponent.test.tsx
import { describe, it, expect } from 'vitest'
import { render, screen } from '@testing-library/react'
import NewComponent from './NewComponent'

describe('NewComponent', () => {
  it('renders without crashing', () => {
    render(<NewComponent />)
    // Add assertions
  })
})
```

## Phase 4: Documentation Check

Read `docs/TESTS.md` and check if:
- New features in changed files are mentioned in docs
- Test documentation needs updates

## Output Format

Present a concise, actionable report:
- Focus ONLY on changed files
- Clear test status indicators (✅ ⚠️ ❌)
- File paths for easy copy-paste
- Immediate action items
- Quick test templates

This is a **fast, targeted check** for pre-commit workflow - not a full audit.

Use TodoWrite to track progress through phases.
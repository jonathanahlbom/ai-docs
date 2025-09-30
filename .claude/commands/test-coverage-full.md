---
description: Full codebase test coverage audit vs documentation
allowed-tools: Read, Glob, Grep, Write, Edit, TodoWrite
---

Perform comprehensive test coverage audit for the entire codebase:

## Phase 1: Read Test Documentation

Read `docs/TESTS.md` to understand what test coverage is documented and expected.

## Phase 2: Discover All Actual Tests

Use Glob to find all test files:
- Playwright E2E tests: `tests/**/*.spec.ts`
- Vitest unit tests: `src/**/*.test.{ts,tsx}` and `src/**/*.spec.{ts,tsx}`

Read each test file to extract:
- Test suite names
- Test descriptions
- What components/features they cover

## Phase 3: Map Entire Codebase

Use Glob to identify all testable code:
- All React components: `src/components/**/*.{tsx,ts}` (exclude .test.tsx, .spec.tsx)
- All pages: `src/pages/**/*.{tsx,ts}` (exclude .test.tsx, .spec.tsx)
- Key utilities: `src/lib/**/*.{ts,tsx}`, `src/hooks/**/*.{ts,tsx}`

Reference `docs/common/file-tree.md` and `docs/ARCHITECTURE.md` to understand critical features.

## Phase 4: Comprehensive Gap Analysis

For EVERY component and page:
1. Check if corresponding test file exists
2. Identify components/pages with NO tests
3. Identify tests that exist but aren't documented in `docs/TESTS.md`
4. Check if documented tests are outdated or missing

Calculate coverage metrics:
- Total components vs tested components
- Total pages vs tested pages
- E2E coverage by user journey
- Critical features without tests

## Phase 5: Generate Comprehensive Report

Present findings with these sections:

### 📊 Coverage Summary
- Total files: X components, Y pages
- Files with tests: X% coverage
- E2E test count
- Unit test count
- Critical gaps count

### ✅ Test Inventory
List ALL existing tests by category:
- **E2E Tests (Playwright)**: List all with descriptions
- **Unit Tests (Vitest)**: List all with components covered

### ❌ Missing Tests (HIGH PRIORITY)
Prioritized list of components/pages WITHOUT tests:
1. **Critical Components** (HeroSection, maps, charts)
2. **User-facing Pages** (Index, Startups, Scaleups, Reports)
3. **Interactive Features** (filters, AI assistant, visualizations)
4. **Utility Components** (buttons, forms, shared components)

### 📝 Documentation Gaps
- Tests that exist but aren't in `docs/TESTS.md`
- Documented tests that are outdated
- Test framework setup not documented

### 🎯 Recommendations
Top 10 most important tests to write next, with:
- File path to create
- What to test
- Test type (E2E vs unit)
- Priority level

## Phase 6: Update Documentation

Update `docs/TESTS.md` to reflect current reality:

```markdown
# Testing Framework - SSN Platform

**Status**: 🔄 Active Development

## Overview
[Brief description of testing strategy]

## Test Frameworks
- **Vitest** - Unit and component testing
- **Playwright** - E2E browser testing
- **React Testing Library** - Component interaction testing

## Current Test Coverage

### E2E Tests (Playwright)
[List all E2E tests with descriptions]

### Unit Tests (Vitest)
[List all unit tests with components covered]

## Running Tests

\`\`\`bash
# Run unit tests
npm run test

# Run unit tests with UI
npm run test:ui

# Run E2E tests
npx playwright test

# Run specific test file
npm run test src/components/Example.test.tsx
\`\`\`

## Coverage Gaps

[Include gap analysis summary]

## Test Writing Guidelines

[Brief guidelines for writing new tests]

## Recommended Next Tests

[Top 10 priority tests from recommendations]
```

## Output Format

Present a well-structured report with:
- Clear sections using markdown headers
- Color indicators: ✅ ❌ ⚠️ 🎯 📊
- File paths for easy navigation
- Actionable next steps
- Updated TESTS.md confirmation

Use TodoWrite to track progress through phases.
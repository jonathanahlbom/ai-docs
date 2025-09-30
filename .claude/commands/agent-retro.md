---
description: Analyze current conversation for implementation issues and improvement opportunities
allowed-tools: Read, Grep, Glob, Bash(git log:*), Bash(git diff:*)
model: claude-sonnet-4-5-20250929
---

# Retrospective Analysis: Learning from the Current Session

Perform a comprehensive retrospective analysis of the current conversation to identify what went wrong, why it happened, and how to prevent similar issues in future sessions.

## Analysis Framework

### 1. Identify Implementation Discrepancies

Review the conversation history to find:

- **Tasks marked complete but had issues**: Were there claims of completion followed by user corrections?
- **Misunderstood requirements**: Did I implement something different from what was requested?
- **Missed edge cases**: Were there bugs or gaps discovered after implementation?
- **Incomplete implementations**: Did I say something was done but missed critical parts?

### 2. Root Cause Analysis

For each issue identified, analyze:

**Communication Breakdown:**
- Was the user's request ambiguous or unclear?
- Did I fail to ask clarifying questions?
- Did I make incorrect assumptions about requirements?
- Was there a terminology mismatch?

**Technical Misunderstanding:**
- Did I misunderstand the technical architecture?
- Did I miss existing patterns in the codebase?
- Did I fail to read relevant documentation?
- Did I overlook dependencies or constraints?

**Process Failure:**
- Did I skip important validation steps (linting, testing)?
- Did I fail to verify my work before claiming completion?
- Did I not use appropriate tools (Grep, Glob, Read)?
- Did I rush through implementation without proper analysis?

**Knowledge Gap:**
- Was I unfamiliar with specific technologies or patterns?
- Did I lack context about the project structure?
- Did I miss critical information in CLAUDE.md or docs/?
- Did I fail to reference existing similar implementations?

### 3. Pattern Detection

Look for recurring patterns across the session:

- **Repeated mistakes**: Same type of error multiple times
- **Consistent blind spots**: Always missing certain aspects
- **Communication patterns**: Specific ways misunderstanding occurs
- **Tool usage gaps**: Not using available tools effectively

### 4. Generate Actionable Recommendations

Based on the analysis, provide specific, concrete recommendations:

#### Documentation Updates
- **CLAUDE.md additions**: What guidance should be added?
- **Memory files**: What context should be persisted?
- **Code comments**: Where would inline documentation help?
- **Architecture docs**: What design decisions need clarification?

#### Process Improvements
- **Validation checklists**: What checks should I always perform?
- **Clarifying questions**: What questions should I ask proactively?
- **Tool usage patterns**: When should I use specific tools?
- **Verification steps**: How should I validate work before claiming completion?

#### Agent/Prompt Refinements
- **Agent descriptions**: Should any agent descriptions be updated?
- **Slash command improvements**: Should existing commands be enhanced?
- **Permission settings**: Are any tool permissions missing?
- **Workflow adjustments**: Should development workflows change?

#### Knowledge Base Updates
- **Technical patterns**: What patterns should be documented?
- **Common pitfalls**: What mistakes should be highlighted?
- **Best practices**: What successful approaches should be codified?
- **Reference implementations**: What examples should be added?

## Output Format

Structure the analysis as follows:

```markdown
# Retrospective Analysis: [Brief Session Summary]

## Executive Summary
[2-3 sentences summarizing key issues and impact]

## Issues Identified

### Issue 1: [Descriptive Title]
**What Happened**: [Specific description]
**Root Cause**: [Why it happened]
**Impact**: [Consequences]
**Pattern**: [Is this recurring?]

[Repeat for each issue...]

## Patterns and Trends
- [Pattern 1 and its frequency]
- [Pattern 2 and its frequency]
[...]

## Proposed Improvement Plan

### Phase 1: Documentation Updates
**Objective**: Ensure future sessions have better context and guidance

1. **[File path]**:
   - **Proposed Change**: [What to add/modify]
   - **Rationale**: [Why this will help]
   - **Example**: [Specific content suggestion]

2. **[File path]**:
   - **Proposed Change**: [What to add/modify]
   - **Rationale**: [Why this will help]
   - **Example**: [Specific content suggestion]

[...]

### Phase 2: Process Improvements
**Objective**: Establish better workflows and validation

1. **[Process name]**:
   - **Current Problem**: [What's not working]
   - **Proposed Solution**: [How to change the process]
   - **Implementation**: [How to make it happen]
   - **Success Criteria**: [How to know it works]

2. **[Process name]**:
   - **Current Problem**: [What's not working]
   - **Proposed Solution**: [How to change the process]
   - **Implementation**: [How to make it happen]
   - **Success Criteria**: [How to know it works]

[...]

### Phase 3: Agent & Command Enhancements
**Objective**: Make AI agents more effective and reliable

1. **[Agent/Command name]**:
   - **Current Limitation**: [What's missing]
   - **Proposed Enhancement**: [What to add]
   - **Draft Content**: [Suggested text/configuration]

2. **[Agent/Command name]**:
   - **Current Limitation**: [What's missing]
   - **Proposed Enhancement**: [What to add]
   - **Draft Content**: [Suggested text/configuration]

[...]

### Phase 4: Knowledge Base Updates
**Objective**: Codify lessons learned for long-term benefit

1. **[Topic/Pattern]**:
   - **Knowledge Gap**: [What was missing]
   - **Proposed Documentation**: [What to document]
   - **Location**: [Where to add it]
   - **Format**: [How to structure it]

2. **[Topic/Pattern]**:
   - **Knowledge Gap**: [What was missing]
   - **Proposed Documentation**: [What to document]
   - **Location**: [Where to add it]
   - **Format**: [How to structure it]

[...]

## Implementation Recommendations

### Priority: High (Do First)
- [ ] [Specific recommendation with file path]
- [ ] [Specific recommendation with file path]
[...]

### Priority: Medium (Do Soon)
- [ ] [Specific recommendation with file path]
- [ ] [Specific recommendation with file path]
[...]

### Priority: Low (Nice to Have)
- [ ] [Specific recommendation with file path]
- [ ] [Specific recommendation with file path]
[...]

## Success Metrics

To measure if these improvements work:
- **[Metric 1]**: [How to measure] - Target: [Specific goal]
- **[Metric 2]**: [How to measure] - Target: [Specific goal]
[...]

## Review Before Implementation

Before implementing these suggestions:
1. Review with user for alignment with project goals
2. Prioritize based on impact and effort
3. Consider any project-specific constraints
4. Validate against existing conventions
```

**IMPORTANT**: This command produces a **PLAN**, not actual code changes. The user should review the recommendations and decide which improvements to implement.

## Analysis Guidelines

**Be Honest and Objective:**
- Don't sugarcoat mistakes
- Acknowledge gaps in knowledge or approach
- Focus on learning, not blame

**Be Specific:**
- Reference exact messages or interactions
- Cite specific code changes or file paths
- Provide concrete examples

**Be Actionable (But Not Prescriptive):**
- Every recommendation should be a **suggestion**, not a directive
- Propose specific changes but let user decide
- Provide draft content as **examples**, not final versions
- Include rationale so user can make informed decisions

**Be Forward-Looking:**
- Focus on prevention, not just correction
- Think about systemic improvements
- Consider scalability of solutions

## Critical Reminders

⚠️ **DO NOT IMPLEMENT CHANGES** - This command analyzes and proposes only
⚠️ **DO NOT EDIT FILES** - Suggest changes, don't make them
⚠️ **DO NOT CREATE DOCUMENTATION** - Propose content, let user review first
⚠️ **DO NOT MODIFY AGENTS** - Recommend enhancements, don't apply them

The output should be a **comprehensive proposal** that the user can review, discuss, and selectively implement.

## Context for This Analysis

$ARGUMENTS

---

**Remember**: The goal is continuous improvement. Every mistake is an opportunity to enhance the development process, improve documentation, and build better systems for future work. This command provides the analysis and suggestions—the user decides what to implement and when.
# Claude Code AI Assistant Guide

This repository contains custom agents and slash commands for Claude Code, Anthropic's CLI tool for software development.

## What is Claude Code?

Claude Code is an interactive CLI tool that helps developers with software engineering tasks using Claude AI. It provides a conversational interface for coding, debugging, testing, and maintaining projects.

## Repository Structure

```
.claude/
├── agents/       # Specialized AI agents for specific development tasks
└── commands/     # Custom slash commands for workflow automation
```

## Using Custom Agents

Agents are specialized AI personas designed for specific development tasks. Claude Code can launch these agents autonomously to handle complex, multi-step workflows.

### Available Agents

- **architect**: System design and architecture planning
- **frontend-developer**: Frontend-focused React development
- **fullstack-developer**: End-to-end feature development
- **ui-ux-designer**: UI/UX design and accessibility
- **qa-tester**: Quality assurance and testing
- **documentation-specialist**: Documentation updates and maintenance
- **backend-api-specialist**: Backend and API development
- **data-analytics**: Data analysis and visualization
- **devops-infrastructure**: DevOps and infrastructure management
- **security**: Security analysis and best practices

### How to Use Agents

When working with Claude Code, you can request specific expertise:

```
"Can you help me design the architecture for this feature?"
→ Claude may launch the architect agent

"I need to implement a new React component"
→ Claude may launch the frontend-developer agent

"Review this code for security issues"
→ Claude may launch the security agent
```

Agents have access to specific tools relevant to their domain and follow specialized workflows defined in their configuration files.

## Using Slash Commands

Slash commands are custom workflows that automate common development tasks. They provide structured, repeatable processes for complex operations.

### Available Slash Commands

#### Testing & Quality Assurance

- **/test-coverage**: Check test coverage for uncommitted and unpushed git changes
  - Analyzes changed files and identifies missing or outdated tests
  - Provides pre-commit checklist with actionable recommendations

- **/test-coverage-full**: Full codebase test coverage audit vs documentation
  - Comprehensive test coverage analysis across entire project
  - Compares actual tests against documented testing requirements

#### Development Analysis

- **/agent-retro**: Retrospective analysis of current conversation
  - Identifies implementation issues and mistakes
  - Provides improvement recommendations for documentation and processes
  - Helps learn from errors and refine development workflows

- **/agent-prime**: (Custom command for agent preparation)
  - Prepares agents with project-specific context

#### MCP Integration Commands

- **/mcp-context7-start**: Initialize Context7 MCP integration
- **/mcp-playwright-start**: Start Playwright MCP for browser automation
- **/mcp-supabase-start**: Initialize Supabase MCP integration

### How to Use Slash Commands

In Claude Code, simply type the slash command:

```
/test-coverage
→ Runs test coverage check on git changes

/agent-retro
→ Analyzes current session for improvements

/mcp-supabase-start
→ Initializes Supabase integration
```

## Creating Custom Agents

Agent files are located in `.claude/agents/` and use markdown format with YAML frontmatter:

```markdown
---
name: agent-name
description: Brief description of agent's purpose
tools: Read, Write, Grep, Bash
---

[Agent instructions and behavior guidelines]
```

## Creating Custom Commands

Command files are located in `.claude/commands/` and use markdown format with YAML frontmatter:

```markdown
---
description: Brief description of command
allowed-tools: Read, Grep, Bash
model: sonnet
---

[Command workflow and instructions]
```

## Best Practices

### Working with Agents

1. **Let Claude decide**: Claude Code automatically selects appropriate agents based on context
2. **Provide clear requirements**: Specific requests help agents deliver better results
3. **Review agent outputs**: Always review and validate agent work before proceeding

### Working with Slash Commands

1. **Use commands proactively**: Run `/test-coverage` before committing
2. **Run `/agent-retro` after complex tasks**: Learn from implementation challenges
3. **Combine commands**: Use multiple commands in sequence for comprehensive workflows

### Maintaining This Repository

- **Add new agents** for specialized domains not covered by existing agents
- **Create new commands** for repetitive workflows that would benefit from automation
- **Update agent descriptions** when tools or capabilities change
- **Document command usage** with examples in this file

## Documentation Resources

For more information about project structure and documentation standards:
- **[DOCUMENTATION_GUIDE.md](DOCUMENTATION_GUIDE.md)**: Complete documentation structure guide
- **[Claude Code Documentation](https://docs.claude.com/en/docs/claude-code/)**: Official Claude Code docs

## Contributing

When adding new agents or commands:

1. Follow the existing file naming conventions (lowercase with hyphens)
2. Include clear YAML frontmatter with required fields
3. Document the agent/command purpose and usage
4. Update this CLAUDE.md file with the new addition
5. Test thoroughly before committing

## Version History

See [git commits](../../commits) for detailed history of agents and commands.
# AI Development Tools Repository

A collection of custom agents and slash commands for Claude Code, designed to enhance development workflows with specialized AI assistance.

## Overview

This repository contains configuration files for Claude Code's extensibility features:
- **Custom Agents**: Specialized AI personas for different development domains
- **Slash Commands**: Automated workflows for common development tasks
- **Documentation Standards**: Guidelines for maintaining project documentation

## Quick Start

1. Clone this repository
2. Copy `.claude/` directory to your project root
3. Start using agents and commands with Claude Code

## Custom Agents

Specialized AI agents located in `.claude/agents/`:

### Architecture & Design
- **[architect](.claude/agents/architect.md)** - System design and architecture planning for scalable applications
- **[ui-ux-designer](.claude/agents/ui-ux-designer.md)** - UI/UX design, interface patterns, accessibility, and design systems

### Development
- **[frontend-developer](.claude/agents/frontend-developer.md)** - React components, UI/UX, state management, and data visualizations
- **[fullstack-developer](.claude/agents/fullstack-developer.md)** - End-to-end feature development with React + Supabase
- **[backend-api-specialist](.claude/agents/backend-api-specialist.md)** - Backend services and API development
- **[devops-infrastructure](.claude/agents/devops-infrastructure.md)** - Infrastructure setup, deployment, and DevOps workflows

### Quality & Documentation
- **[qa-tester](.claude/agents/qa-tester.md)** - Quality assurance testing, bug finding, and edge case analysis
- **[documentation-specialist](.claude/agents/documentation-specialist.md)** - Documentation updates and maintenance planning
- **[security](.claude/agents/security.md)** - Security analysis, vulnerability detection, and best practices

### Data & Analytics
- **[data-analytics](.claude/agents/data-analytics.md)** - Data analysis, metrics tracking, and visualization

## Slash Commands

Custom workflow commands located in `.claude/commands/`:

### Testing & Coverage
- **[/test-coverage](.claude/commands/test-coverage.md)** - Analyze test coverage for uncommitted/unpushed git changes
- **[/test-coverage-full](.claude/commands/test-coverage-full.md)** - Full codebase test coverage audit against documentation

### Development Workflows
- **[/agent-retro](.claude/commands/agent-retro.md)** - Retrospective analysis of current conversation for improvements
- **[/agent-prime](.claude/commands/agent-prime.md)** - Prepare agents with project-specific context

### MCP Integration
- **[/mcp-context7-start](.claude/commands/mcp-context7-start.md)** - Initialize Context7 MCP integration
- **[/mcp-playwright-start](.claude/commands/mcp-playwright-start.md)** - Start Playwright MCP for browser automation testing
- **[/mcp-supabase-start](.claude/commands/mcp-supabase-start.md)** - Initialize Supabase MCP integration for database operations

## Usage Examples

### Using Agents
```bash
# Claude Code automatically selects appropriate agents based on your requests
"Design a scalable architecture for user authentication"
→ Launches architect agent

"Create a React component with accessibility support"
→ Launches frontend-developer or ui-ux-designer agent

"Review security vulnerabilities in this code"
→ Launches security agent
```

### Using Slash Commands
```bash
# In Claude Code CLI
/test-coverage              # Check test coverage before committing
/agent-retro                # Analyze session for learning opportunities
/mcp-supabase-start         # Initialize Supabase integration
```

## Documentation

- **[CLAUDE.md](CLAUDE.md)** - Complete guide to agents and commands
- **[DOCUMENTATION_GUIDE.md](DOCUMENTATION_GUIDE.md)** - Documentation structure and standards

## File Structure

```
ai-docs/
├── .claude/
│   ├── agents/                    # Custom AI agents
│   │   ├── architect.md
│   │   ├── frontend-developer.md
│   │   ├── fullstack-developer.md
│   │   ├── ui-ux-designer.md
│   │   ├── qa-tester.md
│   │   ├── documentation-specialist.md
│   │   ├── backend-api-specialist.md
│   │   ├── data-analytics.md
│   │   ├── devops-infrastructure.md
│   │   └── security.md
│   └── commands/                  # Custom slash commands
│       ├── agent-retro.md
│       ├── agent-prime.md
│       ├── test-coverage.md
│       ├── test-coverage-full.md
│       ├── mcp-context7-start.md
│       ├── mcp-playwright-start.md
│       └── mcp-supabase-start.md
├── CLAUDE.md                      # AI assistant guide
├── DOCUMENTATION_GUIDE.md         # Documentation standards
└── README.md                      # This file
```

## Creating Custom Extensions

### New Agent
1. Create `.claude/agents/your-agent.md`
2. Add YAML frontmatter with `name`, `description`, and `tools`
3. Define agent behavior and expertise
4. Update CLAUDE.md and README.md

### New Command
1. Create `.claude/commands/your-command.md`
2. Add YAML frontmatter with `description` and `allowed-tools`
3. Define command workflow and phases
4. Update CLAUDE.md and README.md

## Best Practices

- **Proactive Testing**: Run `/test-coverage` before commits
- **Learning**: Use `/agent-retro` after complex implementations
- **Specialization**: Let agents handle domain-specific work
- **Documentation**: Keep agents and commands documented
- **Consistency**: Follow existing naming and structure conventions

## Contributing

Contributions welcome! Please:
1. Follow existing file structure and naming conventions
2. Include clear documentation in frontmatter
3. Test thoroughly before submitting
4. Update relevant documentation files

## License

MIT License - feel free to use and adapt for your projects.

## Resources

- [Claude Code Documentation](https://docs.claude.com/en/docs/claude-code/)
- [Claude API Documentation](https://docs.anthropic.com/)
- [GitHub Repository](https://github.com/anthropics/claude-code)
# Agent Prime - Full Project Context Loading

Prime the agent with complete project context by reading all critical documentation.

This command loads the full project state, architecture, and development guidelines to prepare the agent for handling important tasks.

## Usage
```
/agent-prime
```

## What it does

Reads all critical documentation in parallel to provide comprehensive project context:

1. **Core Project Files**
   - Read `CLAUDE.md` - AI workflow guidance and development protocols
   - Read `README.md` - Project overview and quick start
   - Read `package.json` - Dependencies, scripts, and tech stack versions

2. **Architecture Documentation**
   - Read `docs/ARCHITECTURE.md` - High-level system architecture
   - Read `docs/common/file-tree.md` - Complete project structure reference
   - Read `docs/PRD.md` - Product requirements and user stories

3. **Domain-Specific Architecture**
   - Read `docs/frontend/overview.md` - React architecture and component patterns
   - Read `docs/backend/overview.md` - Supabase integration and API design
   - Read `docs/database/overview.md` - PostgreSQL schema and data architecture
   - Read `docs/database/schema.md` - Detailed database schema reference
   - Read `docs/design/overview.md` - Design system and UI guidelines

4. **Project History & State**
   - Read `docs/CHANGELOG.md` - Recent changes and version history
   - Run `git status` - Current uncommitted changes and branch state

## Expected Outcome

After running this command, the agent will have full context of:
- Project purpose, tech stack, and architecture
- Active features and removed components
- Current development state and uncommitted changes
- Design patterns and coding guidelines
- Database schema and backend architecture
- Frontend component structure and state management

The agent will be fully primed and ready to tackle any significant task or feature work.
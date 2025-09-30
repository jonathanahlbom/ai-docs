# Start Supabase MCP Server

Start the Supabase MCP server for database management and backend operations.

## Usage
```
/mcp-supabase-start
```

## What it does
Starts the Supabase MCP server with comprehensive database and project management capabilities.

## Server Configuration
```json
{
  "command": "npx",
  "args": ["-y", "@modelcontextprotocol/server-supabase"],
  "env": {
    "SUPABASE_ACCESS_TOKEN": "your_supabase_access_token_here"
  }
}
```

## Available Tools After Start

### Documentation & Search
- `mcp__supabase__search_docs` - Search Supabase documentation

### Organization & Project Management
- `mcp__supabase__list_organizations` - List user organizations
- `mcp__supabase__get_organization` - Get organization details
- `mcp__supabase__list_projects` - List all Supabase projects
- `mcp__supabase__get_project` - Get project details
- `mcp__supabase__create_project` - Create new project
- `mcp__supabase__pause_project` - Pause project
- `mcp__supabase__restore_project` - Restore project

### Database Operations
- `mcp__supabase__list_tables` - List database tables
- `mcp__supabase__list_extensions` - List database extensions
- `mcp__supabase__list_migrations` - List migrations
- `mcp__supabase__apply_migration` - Apply database migration
- `mcp__supabase__execute_sql` - Execute raw SQL queries
- `mcp__supabase__generate_typescript_types` - Generate TS types

### Edge Functions
- `mcp__supabase__list_edge_functions` - List Edge Functions
- `mcp__supabase__get_edge_function` - Get Edge Function code
- `mcp__supabase__deploy_edge_function` - Deploy Edge Function

### Branch Management (Pro/Teams)
- `mcp__supabase__create_branch` - Create development branch
- `mcp__supabase__list_branches` - List project branches
- `mcp__supabase__delete_branch` - Delete branch
- `mcp__supabase__merge_branch` - Merge branch to production
- `mcp__supabase__reset_branch` - Reset branch migrations
- `mcp__supabase__rebase_branch` - Rebase branch on production

### Project Configuration
- `mcp__supabase__get_project_url` - Get project API URL
- `mcp__supabase__get_anon_key` - Get anonymous API key
- `mcp__supabase__get_logs` - Get project logs
- `mcp__supabase__get_advisors` - Get security/performance advisors
- `mcp__supabase__get_cost` - Get cost estimates
- `mcp__supabase__confirm_cost` - Confirm cost for operations

## Requirements
- Supabase account and access token
- Internet connection for API calls
- Node.js and npm installed

## Setup
1. Get your Supabase access token from the Supabase dashboard
2. Set the `SUPABASE_ACCESS_TOKEN` environment variable
3. Run the command to start the MCP server
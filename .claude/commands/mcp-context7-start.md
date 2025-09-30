# Start Context7 MCP Server

Start the Context7 MCP server for accessing up-to-date code documentation and examples.

## Usage
```
/mcp-context7-start
```

## What it does
Starts the Context7 MCP server with the following capabilities:
- Provides up-to-date code documentation for various libraries
- Pulls version-specific documentation directly into AI prompts
- Helps prevent hallucinated or outdated code generation
- Access to real-time, accurate code examples and best practices

## Server Configuration
```json
{
  "command": "npx",
  "args": ["-y", "@upstash/context7-mcp"],
  "env": {
    "CONTEXT7_API_KEY": "your_api_key_here_optional"
  }
}
```

## How to Use
After starting the server, simply mention "use context7" in your prompts to:
- Get current documentation for libraries and frameworks
- Access version-specific code examples
- Ensure accurate, non-hallucinated code suggestions

## Configuration Notes
- **API Key is optional** - Higher rate limits available with key from context7.com/dashboard
- **Node.js v18.0.0+** required
- Works with remote server: `https://mcp.context7.com/mcp`

## Available Tools After Start
- Documentation search and retrieval tools
- Version-specific code example access
- Real-time library documentation queries

## Requirements
- Node.js v18.0.0 or higher
- Internet connection for documentation API
- Optional: Context7 API key for higher rate limits

## Getting an API Key (Optional)
1. Visit https://context7.com/dashboard
2. Sign up for an account
3. Generate an API key
4. Add to environment: `CONTEXT7_API_KEY=your_key`
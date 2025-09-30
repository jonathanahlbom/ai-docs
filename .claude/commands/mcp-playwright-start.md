# Start Playwright MCP Server

Start the Playwright MCP server for browser automation and testing capabilities.

## Usage
```
/mcp-playwright-start
```

## What it does
Starts the Playwright MCP server with the following capabilities:
- Browser automation (navigate, click, type, etc.)
- Page snapshots and screenshots
- Form filling and interaction
- Console message monitoring
- Network request tracking
- File uploads
- Browser tab management

## Server Configuration
```json
{
  "command": "npx",
  "args": ["-y", "@modelcontextprotocol/server-playwright"],
  "env": {
    "PLAYWRIGHT_BROWSERS_PATH": "~/.cache/ms-playwright"
  }
}
```

## Available Tools After Start
- `mcp__playwright__browser_navigate`
- `mcp__playwright__browser_click` 
- `mcp__playwright__browser_snapshot`
- `mcp__playwright__browser_close`
- `mcp__playwright__browser_install`
- `mcp__playwright__browser_evaluate`
- `mcp__playwright__browser_console_messages`
- `mcp__playwright__browser_wait_for`
- `mcp__playwright__browser_take_screenshot`
- `mcp__playwright__browser_resize`
- And many more browser automation tools
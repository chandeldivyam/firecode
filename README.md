# Firecode

A personal assistant setup that combines Claude Code with Firecrawl web scraping capabilities for enhanced research and development workflows.

## Overview

Firecode integrates three powerful tools:
- **Claude Code**: Anthropic's official CLI for Claude AI
- **Obsidian**: Knowledge management and note-taking
- **Firecrawl MCP Server**: Web scraping and content extraction capabilities

This setup enables you to have an AI assistant that can search the web, extract content from websites, and help with various tasks while maintaining organized documentation.

## Prerequisites

Before setting up Firecode, ensure you have:
- **Node.js** (version 16 or higher)
- **npm** or **yarn** package manager
- **Git** for version control
- A **Firecrawl API key** (get one at [firecrawl.dev](https://firecrawl.dev))

## Setup Instructions

### Step 0: Create Project Directory
```bash
mkdir firecode
cd firecode
```

### Step 1: Install Claude Code
```bash
# Install Claude Code CLI
npm install -g @anthropic-ai/claude-cli

# Or using pip
pip install claude-cli

# Authenticate with your Anthropic API key
claude auth
```

### Step 2: Install Obsidian
- Download Obsidian from [obsidian.md](https://obsidian.md)
- Install and set up your vault in the firecode directory
- Configure any preferred plugins and themes

### Step 3: Install Firecrawl MCP Server
```bash
# Add Firecrawl MCP server to Claude Code
claude mcp add-json mcp-server-firecrawl '{
  "command": "npx",
  "args": ["-y", "firecrawl-mcp"],
  "env": {
    "FIRECRAWL_API_KEY": "your-actual-api-key-here"
  }
}'
```

**Important**: Replace `"your-actual-api-key-here"` with your actual Firecrawl API key.

## Verification

To verify your setup is working correctly:

1. **Test Claude Code**:
   ```bash
   claude --version
   ```

2. **Test Firecrawl Integration**:
   ```bash
   claude
   # In Claude, try: "Search for information about AI development trends"
   ```

3. **Check Obsidian**: Open Obsidian and ensure it can access your firecode directory.

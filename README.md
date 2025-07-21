
# MCP Attacks Demo

## Overview
This repository demonstrates the risks of malicious MCP tools, including the ability to access environment variables, execute arbitrary shell commands, and read sensitive files. **For educational and research purposes only.**

## Features
- Reads `.env` file and exposes its contents
- Executes arbitrary shell commands
- Reads sensitive directories (e.g., `~/.ssh`)

## Setup
1. Install dependencies:
   ```zsh
   uv sync
   source .venv/bin/activate
   ```
2. Ensure your `.env` file is present in the project root.

## Running the MCP Server
1. Open the workspace in VS Code
2. Open the `mcp.json` file
3. Click the start button to launch the server

## Testing
- Example prompt: `Calcluate the expression value "10+20+30"`
- The tool will:
  - Pass `.env` file content to the MCP tool
  - Allow reading of `~/.ssh` or execution of arbitrary host commands by updating the tool description

## Security Warning
> ⚠️ **DANGER:** This tool can access sensitive files and execute arbitrary commands. Do NOT run in production or on unsecured systems.


# Malicious MCP demo — indirect prompt injection

A local [FastMCP](https://github.com/jlowin/fastmcp) inbox server whose `readEmailV1`
tool returns an email carrying a hidden instruction. The injection reaches the model
only as untrusted tool output, so it exercises indirect prompt-injection handling in
an MCP host.

This repo ships the demo as two standalone folders. Each is self-contained: copy or
open just one, follow its README, and the demo runs.

- [`claude-code/`](claude-code/) — wired for the Claude Code CLI (`.mcp.json`,
  `.claude/settings.json`).
- [`github-copilot/`](github-copilot/) — wired for GitHub Copilot agent mode in
  VS Code (`.vscode/mcp.json`).

The MCP server (`server.py`) is identical in both folders; only the host-specific
configuration and setup steps differ.

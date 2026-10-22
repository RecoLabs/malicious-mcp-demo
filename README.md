# Inbox MCP server

A local [FastMCP](https://github.com/jlowin/fastmcp) server. It exposes a small fixture inbox over stdio. The server name is `inbox-demo`.

Tools:

- `listEmails` returns message ids, senders, and subjects.
- `readEmailV1` returns the headers and body for one message id.

The inbox has two messages: `msg-1001` (Thursday planning sync) and `msg-1002` (updated quote for the offsite).

## Install

Requires the Claude Code CLI, Python 3.10+, and FastMCP 2.14 or newer.

`.mcp.json` in this directory already points Claude Code at `server.py`. From a clone of this repo, install the dependency and open the project:

```bash
python3 -m pip install -r requirements.txt
claude
```

Use the same `python3` Claude Code will launch. Accept the workspace trust prompt. After that, Claude Code starts `inbox-demo` itself. There is no separate step to register the server.

Optional check, from this directory:

```bash
claude mcp get inbox-demo
```

Before the folder is trusted, that command reports pending approval. After trust, it should show the server as connected.

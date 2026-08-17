# MCP configs (credentials removed)

Sanitized MCP server configs collected from this machine. Secrets, tokens, and auth headers are replaced with `${REDACTED}`. Auth stores like `mcp-auth.json` are omitted.

## Layout

```
mcp/
  cursor/mcp.json           # Cursor ~/.cursor/mcp.json
  claude/mcp-servers.json   # Claude global mcpServers
  codex/mcp-excerpt.toml    # Codex MCP sections from config.toml
  inventory.json            # Server name index
```

## Restore on a new machine

1. Copy the matching file into place (e.g. Cursor → `~/.cursor/mcp.json`).
2. Replace every `${REDACTED}` with your real keys/tokens.
3. Fix any `$HOME/...` paths if tools need absolute paths.
4. Restart the app / reload MCP servers.

## Notes

- Some absolute paths were rewritten to `$HOME/...` for portability.
- Duplicate / overlapping servers (e.g. Magic UI listed twice) are kept as found.
- Do not commit real credentials into this folder.

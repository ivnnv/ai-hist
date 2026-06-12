# ai-hist-mcp

Thin `npx` wrapper for the [`ai-hist`](https://www.npmjs.com/package/ai-hist) stdio MCP server.

```bash
npx -y ai-hist-mcp
```

The wrapper depends on `ai-hist` and launches its `ai-hist/mcp-server` export. It preserves the same environment contract:

- `AI_HIST_DB` points to the ai-hist SQLite database.
- `TRAJECTORY_ROOT` points to the root containing `**/compacted/*.json` trajectory files.

Project scoping is configured with CLI args:

```bash
npx -y ai-hist-mcp --project .
npx -y ai-hist-mcp --project /path/to/project
```

Both forms restrict all MCP tools to one project path, including child paths.

The MCP server exposes:

- `search_history`
- `recent_entries`
- `get_session`
- `get_context`
- `stats`
- `search_trajectories`
- `why_for_task`

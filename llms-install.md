# Installing Park Graph in Cline

Park Graph is a remote MCP server at https://parkgraph.com/api/mcp. There is nothing to clone, build or run, and no API key.

## Set up

Add this entry to Cline's MCP settings file (`cline_mcp_settings.json`), inside `mcpServers`, keeping any servers already there:

```json
{
  "mcpServers": {
    "park-graph": {
      "type": "streamableHttp",
      "url": "https://parkgraph.com/api/mcp",
      "disabled": false,
      "autoApprove": []
    }
  }
}
```

Save the file. The server lists 8 tools: search_lots, get_lot, quote, reserve, get_session, extend_session, my_sessions, my_vehicles.

## Check it works

Call `search_lots` with lat 47.674 and lng -122.122 (downtown Redmond, Washington). It returns at least one lot, 16300 Redmond Way.

## Notes

- my_sessions and my_vehicles are for a driver signed in to Park Graph. Without sign-in they answer 401 with the sign-in details; the other tools need no sign-in.
- Payment always completes on parkgraph.com with the driver present; no tool charges money on its own.
- reserve and extend_session are marked destructive: they hold a space or price more time. Don't add them to `autoApprove`.
- Docs: https://parkgraph.com/developers/mcp. Support: support@parkgraph.com.

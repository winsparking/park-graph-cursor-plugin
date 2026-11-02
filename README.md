# Park Graph for Cursor

Find, price and hold parking at Park Graph lots from Cursor: search lots near a place, get quotes, hold a space and check or extend a session. Payment always completes on parkgraph.com.

## Install

Install from the Cursor Marketplace, or add this to your Cursor MCP settings:

```json
{
  "mcpServers": {
    "park-graph": {
      "url": "https://parkgraph.com/api/mcp"
    }
  }
}
```

No API key or configuration is needed.

## Tools

- `search_lots`: Find Park Graph lots near a place, nearest first, with spaces left and current price
- `get_lot`: Full public details for one lot
- `quote`: Price to park at a lot for a number of hours
- `reserve`: Hold a space for a few minutes; the driver pays on parkgraph.com
- `get_session`: Check a parking session
- `extend_session`: Add time to an active hourly session

## Example prompts

- "Find parking near Coors Field for 3 hours tonight"
- "How much is 2 hours at the nearest Park Graph lot to Union Station, Denver?"
- "Hold a space for me at that lot"

## Links

- Docs: https://parkgraph.com/developers/mcp
- Server: https://parkgraph.com/api/mcp

Maintained by Wins Parking, LLC.

<!-- SETUP_INCOMPLETE -->
# Data sources

The engine works out of the box using **built-in web search and fetch**, which need no
setup. If you connect more powerful tools later, turn them on here and the engine will
prefer them for that kind of data.

To connect a tool, you add it as an MCP server in Claude Code. See
[docs/troubleshooting.md](../docs/troubleshooting.md) for how. Then change `off` to `on`.

## Toggles

| Source | Status | Used for |
|---|---|---|
| Built-in web (search + fetch) | on | Always available. SERP scans, competitor pages, research. |
| Ahrefs MCP | off | Keyword volume, parent topic, related terms, SERP data |
| Google Search Console MCP | off | Your real queries, impressions, positions |
| Google Analytics MCP | off | Traffic and conversion data for your pages |

Change a value to `on` only after you have connected that tool. The engine will never
invent metrics it cannot retrieve. If a source is `off`, it uses the built-in web
fallback and tells you when a number is an estimate rather than measured data.

Run `/setup` to confirm these, or edit them by hand and delete the SETUP_INCOMPLETE line.

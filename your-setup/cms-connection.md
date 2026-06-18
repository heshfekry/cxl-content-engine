<!-- SETUP_INCOMPLETE -->
# CMS connection

By default, the engine hands you a clean document to copy and paste into your CMS. That
works everywhere and needs no setup.

If you want, you can connect your CMS so the engine publishes drafts straight to it. This
is optional and you can do it any time.

## Status

```
status: not_set
last_prompted: none
cms: none
```

- `status` is one of: `not_set`, `connected`, or `later`.
- If `later`, the engine will check in once a week to ask if you want to connect now.
- `cms` is the platform once connected (for example `wordpress`, `webflow`).

## Supported targets

You can connect any CMS that offers an MCP server or an API. Common ones:

- **WordPress** (via the WordPress MCP or REST API)
- **Webflow** (via the Webflow MCP)
- **Ghost, Contentful, Sanity, others** (via their API or an MCP, if available)

Run `/setup` and it will ask whether you want to connect now or later. To connect later,
just say so when the weekly reminder appears, or run `/setup` again.

# Yapp

**Publish a webpage to a live URL, straight from your AI.**

[yapp.page](https://yapp.page) is a hosted [Model Context Protocol](https://modelcontextprotocol.io) server. Connect it to your AI, ask it to build and publish a page, and you get back a live, shareable link in seconds. It handles HTML, PDFs, ZIP sites, images and landing pages, and you can update, password-protect, set an expiry, attach a custom domain, or read form submissions just by asking.

It runs as a remote server, so there's nothing to install or run locally. You sign in with your account (OAuth), or use a token for terminal clients. Free to start.

> This repository is the public home and docs for the hosted yapp.page service. The server runs at `https://yapp.page/mcp`, so there's nothing to clone or run here.

## Endpoint

```
https://yapp.page/mcp
```

Transport: Streamable HTTP. Auth: OAuth 2.1, per user (each person's pages go to their own account).

## Connect

Full setup for every client is at [yapp.page/mcp](https://yapp.page/mcp).

- **Claude (web & desktop):** Settings, then Connectors, then "Add custom connector". Paste `https://yapp.page/mcp` and sign in. Open a new chat and switch the connector on with the + button.
- **ChatGPT** (Developer Mode): Settings, then Apps & Connectors, then "Create app". Set the MCP Server URL to `https://yapp.page/mcp` and Authentication to OAuth.
- **Claude Code:** `claude mcp add --transport http yapp https://yapp.page/mcp`
- **Cursor:** Settings, then MCP, then add an `http` server with the URL `https://yapp.page/mcp`.
- **Codex CLI:** create a Personal Access Token at [Settings, then Connect AI clients](https://yapp.page/settings#tokens), then run `codex mcp add yapp --url https://yapp.page/mcp --bearer-token-env-var YAPP_TOKEN`.

## Tools

| Tool | What it does |
| --- | --- |
| `publish_page` | Publish HTML with optional assets, and get a live URL plus an edit key |
| `update_page` | Replace a page's content, keeping the same URL |
| `delete_page` | Permanently delete a page |
| `get_page_stats` | Views, traffic and referrers |
| `list_my_pages` | List the pages on your account |
| `rename_page` | Change a page's display name |
| `change_page_slug` | Change a page's URL slug |
| `set_page_expiry` | Set days until delete, or never expire |
| `set_page_password` | Add or remove a page password |
| `list_submissions` | Read form submissions captured on a page |
| `add_custom_domain` | Attach a custom domain (Pro and Team) |
| `list_custom_domains` | List attached custom domains |
| `check_custom_domain` | Check a custom domain's DNS and SSL status |
| `remove_custom_domain` | Detach a custom domain |

## Links

- Website: https://yapp.page
- Connect and docs: https://yapp.page/mcp
- Smithery listing: https://smithery.ai/server/yapp/page
- Privacy: https://yapp.page/privacy
- Terms: https://yapp.page/terms

---

Operated by Reamber GmbH (Austria). See the [Impressum](https://yapp.page/impressum).

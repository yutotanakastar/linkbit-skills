---
name: linkbit
description: Shorten URLs, create bulk links, QR codes, and click analytics with LinkBit via MCP or REST API.
---

# LinkBit

Use LinkBit to create short links (`linkbit.live/...`), QR codes, and click stats.

## Setup

1. Create an API key at https://linkbit.live (API Keys page) — key starts with `slk_`.
2. Prefer MCP when available:

```bash
npx -y linkbit-mcp
```

Environment: `APP_URL=https://linkbit.live` and `API_KEY=slk_...`.

Claude Code:

```bash
claude mcp add linkbit -e API_KEY=slk_your_key -e APP_URL=https://linkbit.live -- npx -y linkbit-mcp
```

Install this skill marketplace:

```bash
claude plugin marketplace add yutotanakastar/linkbit-skills
```

## When to use

- User asks to shorten a URL, add UTM, or pick a custom slug
- Bulk shorten several destinations
- QR for print or screen
- Clicks / countries / devices for a link id
- Disable or delete a short link

## MCP tools

| Tool | Use |
| --- | --- |
| `shorten_url` | One link; optional slug + UTM |
| `shorten_urls` | Bulk |
| `list_links` | Newest first |
| `update_link` / `disable_link` / `delete_link` | Manage |
| `get_qr` | PNG or SVG |
| `get_link_stats` / `get_analytics` | Metrics |

## REST (n8n / scripts)

```
Authorization: Bearer slk_...
# or x-api-key: slk_...

POST https://linkbit.live/api/v1/links
POST https://linkbit.live/api/v1/links/bulk
GET  https://linkbit.live/api/v1/links
GET  https://linkbit.live/api/v1/links/:id/stats
GET  https://linkbit.live/api/v1/analytics
```

Docs: https://linkbit.live/docs · MCP page: https://linkbit.live/mcp

## Rules

- Never invent or log the user's `slk_` key.
- Do not overwrite existing `utm_*` query params on the destination unless asked.
- Keep URL fragments (`#...`).
- On 401/400, explain: missing key, slug taken, daily create limit, or unsafe destination.

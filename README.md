# LinkBit Claude skills

Claude Code marketplace for LinkBit: short links, QR codes, and analytics via MCP.

Public install:

```bash
claude plugin marketplace add yutotanakastar/linkbit-skills
```

Or MCP only:

```bash
claude mcp add linkbit -e API_KEY=slk_your_key -e APP_URL=https://linkbit.live -- npx -y linkbit-mcp
```

Create a key at https://linkbit.live → API Keys · Docs: https://linkbit.live/mcp

## Contents

| Path | Description |
| --- | --- |
| [`skills/linkbit/SKILL.md`](./skills/linkbit/SKILL.md) | Shorten links, QR, analytics via MCP/REST |
| [`.claude-plugin/marketplace.json`](./.claude-plugin/marketplace.json) | Marketplace manifest |

## Topics (GitHub)

For skills.sh / Claude marketplace aggregators, this repo should be tagged:

`agent-skills` · `claude-code` · `claude-marketplace` · `mcp` · `mcp-server` · `ai-agents` · `skills`

## License

MIT

# LinkBit Claude skills

Public Claude plugin marketplace for [LinkBit](https://linkbit.live).

## Install

```bash
claude plugin marketplace add yutotanakastar/linkbit-skills
```

Or use MCP directly:

```bash
claude mcp add linkbit -e API_KEY=slk_your_key -e APP_URL=https://linkbit.live -- npx -y linkbit-mcp
```

Create a key at https://linkbit.live → API Keys.

## Contents

| Path | Description |
| --- | --- |
| [`skills/linkbit/SKILL.md`](./skills/linkbit/SKILL.md) | Shorten links, QR, analytics via MCP/REST |
| [`.claude-plugin/marketplace.json`](./.claude-plugin/marketplace.json) | Marketplace manifest |

## License

MIT

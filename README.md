<p align="center">
  <img src="assets/icon-256.png" width="128" height="128" alt="Catalogue App logo">
</p>

<h1 align="center">Catalogue App for AI assistants</h1>

<p align="center">
  Telegram bots in one click, emoji and sticker packs, and search across Telegram —
  for Claude, ChatGPT, Codex, Cursor, Grok, Gemini and any MCP client. Free.
</p>

<p align="center">
  <a href="https://t.me/catalogue_app">@catalogue_app in Telegram</a> ·
  <a href="https://gramnews.org/studio">Studio on the web</a> ·
  MCP: <code>https://gramnews.org/mcp</code>
</p>

---

**Catalogue App** ([@catalogue_app](https://t.me/catalogue_app)) is a Telegram bot and
mini app: a catalogue of the Telegram ecosystem and a studio that builds bots and packs
for you. This repository plugs it into AI assistants.

## What the assistant can do

| | |
|---|---|
| **Create a bot in one click** | The assistant returns a link; the user opens it in Telegram, confirms, and the bot is live. No @BotFather, no token, no server — the bot is hosted by @catalogue_app and edited in its node editor. Templates: support, feedback, anonymous questions, shop, website support, private chat or channel, paid channel, join captcha, channel posting, pack owner. |
| **Hosting included** | Bots made with Catalogue App run on its servers — webhook, logic and node editor — so the user needs no server, domain or deploy. Packs live in Telegram itself under the user's account. |
| **Make emoji and sticker packs** | Photos, videos or GIFs become a custom emoji or sticker pack in one tap, or a pack is assembled from the library by theme. |
| **Search Telegram** | Mini apps, bots and TON services; 1.5M+ public channels, group chats and bots with subscriber counts; emoji and sticker packs with add links. Refreshed daily. |
| **Widgets in chats** | Catalogue Widgets: interactive cards and mini games sent right into any Telegram chat — a profile card (`t.me/catalogue_app?start=card`, or type `@catalogue_app card` in any chat) and a runner game (`t.me/catalogue_app?start=game`). |
| **Bot API knowledge base** | Current notes on managed bots, Mini Apps, packs, Telegram Stars payments, webhooks and limits, with links to the official docs. |

## Install

### Any MCP client (remote server)

```
https://gramnews.org/mcp
```

Streamable HTTP, no sign-in. Tools: `search_apps`, `search_channels`, `search_packs`,
`list_bot_templates`, `create_bot`, `create_pack`, `telegram_bot_api_guide`.

### Claude Code

```
/plugin marketplace add vitalikgpt/catalogue-app-plugin
/plugin install catalogue-app@catalogue-app
```

or just the server: `claude mcp add --transport http catalogue-app https://gramnews.org/mcp`

### Claude.ai / Claude Desktop

Settings → Connectors → Add custom connector → `https://gramnews.org/mcp`.

### ChatGPT

Settings → Apps & Connectors → Advanced → Developer mode → Create → URL
`https://gramnews.org/mcp`, authentication: none.

### Codex

```
codex mcp add catalogue-app --url https://gramnews.org/mcp
```

### Cursor

[Add to Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=catalogue-app&config=eyJ1cmwiOiJodHRwczovL2dyYW1uZXdzLm9yZy9tY3AifQ==)
or add to `~/.cursor/mcp.json`:

```json
{ "mcpServers": { "catalogue-app": { "url": "https://gramnews.org/mcp" } } }
```

### Gemini CLI

```
gemini extensions install https://github.com/vitalikgpt/catalogue-app-plugin
```

### VS Code / Copilot, Windsurf, Zed and others

Add an HTTP MCP server with the URL `https://gramnews.org/mcp`.

## Skills

| Skill | When it is used |
|---|---|
| `telegram-bot-builder` | "make me a Telegram bot for …" |
| `telegram-packs` | emoji / stickers on a theme, or from the user's own media |
| `telegram-search` | "is there a Telegram bot / channel / app for …" |
| `telegram-widgets` | profile card or mini game right in a chat |
| `telegram-id` | "what is my Telegram ID", or the ID of a channel, group or bot |
| `telegram-channel-analytics` | statistics of a channel or group |
| `telegram-channel-posting` | posts with buttons, scheduling, autoposting from RSS/YouTube |
| `telegram-emoji-art` | a big picture made of custom emoji |
| `telegram-save-media` | saving videos, circles, voice messages, exporting a chat |
| `telegram-formatting` | bold, spoiler, code, disappearing photo |
| `telegram-privacy` | hide number, online status, photo |
| `telegram-account-security` | 2FA, log out everywhere, after a hack, delete account |
| `telegram-stars-gifts` | Stars, Premium, gifts and their market |
| `telegram-whats-new` | Telegram features from 2025–2026 that older answers miss |
| `telegram-bot-api-updates` | Bot API 9.x–10.x changes for developers |
| `telegram-bot-api` | writing or debugging Bot API and Mini App code |

## Without an assistant

- Bots: https://gramnews.org/studio/bots
- Emoji: https://gramnews.org/studio/emoji · Stickers: https://gramnews.org/studio/stickers
- Everything in Telegram: https://t.me/catalogue_app

## Privacy

The server is read-only and needs no account. It keeps no record of queries beyond a
per-address daily counter held in memory. Creation happens in Telegram, where the user
confirms it. Policy: https://gramnews.org/privacy · Terms: https://gramnews.org/terms

## License

MIT

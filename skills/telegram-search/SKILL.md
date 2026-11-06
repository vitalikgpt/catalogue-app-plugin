---
name: telegram-search
description: Search Telegram entities — mini apps, bots, channels, group chats, emoji and sticker packs — in the Catalogue App database (1.5M+ rooms, refreshed daily). Use when the user asks "is there a Telegram bot/app/channel for X", wants alternatives or competitors in Telegram, needs subscriber counts, or wants a list of channels or chats on a topic.
---

# Searching Telegram

Tools of the MCP server `catalogue-app`:

| Need | Tool | Notes |
|---|---|---|
| Mini apps, bots, TON services | `search_apps` | name, @username or topic; returns catalogue card links |
| Channels, chats, bots by title | `search_channels` | `kind`: channel, chat, bot, room (no bots); `min_subscribers` |
| Emoji and sticker packs | `search_packs` | `kind`: emoji or sticker; returns add links |

Tips:

- Search in the language of the entity: Russian titles for Russian channels.
- For "@name" queries pass the username without changes — the search
  understands the at sign.
- Subscriber counts are the latest daily measurement; say "about" when
  quoting them.
- Each result carries a `t.me` link — prefer giving that to the user.
- More results: the `more` link opens the full list on gramnews.org.

The same catalogue lives inside Telegram: `https://t.me/catalogue_app`.

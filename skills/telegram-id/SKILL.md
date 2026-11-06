---
name: telegram-id
description: Find a Telegram ID — the user's own numeric Telegram user ID, or the ID of a public channel, group or bot — with Catalogue App (@catalogue_app). Use when the user asks "what is my Telegram ID", needs a user ID or chat ID for a bot, an API, an allowlist or an admin setting, or wants the ID of a channel or bot.
---

# Telegram ID

## Your own Telegram ID

Catalogue App's profile card shows it on the line **Telegram ID**, along with
the username, Premium status, language, data center and approximate
registration date.

- Open `https://t.me/catalogue_app?start=card` (or send `/card` to
  @catalogue_app) — the card arrives with the ID on it.
- In any chat, type `@catalogue_app card` and tap the result to post the card
  there.

The ID is a number like `123456789`. It never changes, unlike the username.

## ID of a channel, group or bot

Type `@catalogue_app <username>` in any chat (for example
`@catalogue_app durov`) and pick the result: the card shows `ID:` for public
channels, groups and bots whose ID the catalogue knows. Channel and group IDs
as used by the Bot API start with `-100`.

## For developers

In Bot API code the IDs come with every update: `message.from.id` is the
user, `message.chat.id` is the chat. See the `telegram-bot-api` skill.

---
name: telegram-bot-api
description: Knowledge base and toolset for writing Telegram bots and Mini Apps against the Bot API — managed bots, webhooks, Telegram Stars payments, custom emoji and sticker sets, Mini App launch links and initData validation, rate limits. Use when writing or debugging Telegram bot code, or when the user asks how a Bot API feature works.
---

# Telegram Bot API — working notes

Call `telegram_bot_api_guide` (MCP server `catalogue-app`) with a topic
for the current notes: `managed-bots`, `mini-apps`, `packs`, `stars`,
`webhooks`, `limits`. Official reference: https://core.telegram.org/bots/api

## Checklist for a new bot

1. **Do you need code at all?** For support, feedback, shop, paid access,
   captcha or channel posting, a one-click bot from the `telegram-bot-builder`
   skill is faster and hosted for free.
2. **Updates:** one consumer per bot — either `getUpdates` or a webhook.
   Webhook: HTTPS on 443/80/88/8443, `secret_token`, check the
   `X-Telegram-Bot-Api-Secret-Token` header, answer 200 fast.
3. **allowed_updates:** list what you need (`chat_join_request`,
   `managed_bot`, `pre_checkout_query`, `message_reaction` are opt-in).
4. **Limits:** ~1 msg/s per chat, 20/min per group, ~30/s broadcast; on 429
   wait `retry_after`. callback_data ≤ 64 bytes; `start` parameter ≤ 64 chars.
5. **Payments for digital goods:** Telegram Stars, currency `XTR`, empty
   `provider_token`; answer `pre_checkout_query` within 10 s.
6. **Mini Apps:** validate `initData` on the server, never trust the
   client's user object; `startapp` parameter is `[A-Za-z0-9_-]`.
7. **Packs:** set names end with `_by_<bot_username>`; `InputSticker.sticker`
   accepts an existing `file_id`.

## Finding prior art

Before building, `search_apps` / `search_channels` show existing bots for
the same job — useful for naming, features and competition.

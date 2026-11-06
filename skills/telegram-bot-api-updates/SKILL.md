---
name: telegram-bot-api-updates
description: Recent Telegram Bot API changes (versions 9.x–10.x, 2025–2026) that older code samples and models miss — managed bots, guest and business bots without Premium, join-request mini apps, rich messages and tables, coloured and inline buttons, ephemeral bot messages, removing other users' reactions, draft streaming, Mini App origin hardening, Log In with Telegram over OIDC. Use when writing or reviewing Telegram bot or Mini App code, when an API call "doesn't exist", or when a Telegram login widget or Mini App in an iframe breaks.
---

# Bot API: what changed recently

Always check the live changelog before relying on memory:
https://core.telegram.org/bots/api-changelog — then the method page.

| Version / date | Change | Practical note |
|---|---|---|
| 9.1 (Jul 2025) | Checklists | New message type |
| 9.2 (Aug 2025) | Channel direct messages, suggested posts | Bots can handle suggested posts |
| 9.3–9.5 | Streaming message drafts, date entities, custom emoji from bots, coloured buttons (9.4) | Stream long AI answers as a draft |
| 9.6 (Apr 2026) | Managed bots | Manager bot with bot management enabled in @BotFather; link `t.me/newbot/<manager>/<username>`; manager receives `managed_bot` and fetches the token. Docs: core.telegram.org/api/bots/managed-bots |
| 10.0 (May 2026) | Business/guest bots without Premium; bot-to-bot messages; `deleteMessageReaction`, `deleteAllMessageReactions` | Users connect bots via Settings → Chat Automation. Admin bots with `can_delete_messages` can remove other people's reactions — one, or up to 10 000 recent ones of a user (`user_id`) or chat (`actor_chat_id`); subscribe to `message_reaction` in `allowed_updates` |
| 10.1 (Jun 2026) | `answerChatJoinRequestQuery`, `sendChatJoinRequestWebApp` | Captcha or quiz mini app before approving a join request |
| 10.1–10.3 (Jun–Aug 2026) | `sendRichMessage` with tables/headings; ephemeral messages in groups; buttons inside text, disabled buttons | Replies visible to one member of a group |
| 10.2 (Jul 2026) | Mini App origin hardening | Telegram.WebApp methods refuse calls from foreign origins; a Mini App inside an iframe breaks — can be relaxed in @BotFather |

## Log In with Telegram

Since March 2026 login is OpenID Connect: `oauth.telegram.org`, PKCE, verify
the `id_token` against the published JWKS. The old HMAC `data-check-string`
widget moved to a legacy path — do not generate it for new sites.
Docs: https://core.telegram.org/bots/telegram-login

## Fastest path for common bots

Support, feedback, shop, captcha, channel posting: a ready managed bot from
`telegram-bot-builder` needs no code or server.

---
name: telegram-group-moderation
description: Moderate a Telegram group or channel for free with @catalogue_app — delete service messages ("joined", "left", "pinned"), captcha for join requests, antiflood, filters for links, swearing, forwards and custom stop words, kick bots added by members, welcome message, rules, and admin commands /ban /mute /warn /kick /del /purge /pin. Use when the user asks for a Telegram moderation bot, antispam, how to remove join/leave messages, a captcha bot, or an alternative to Rose, Combot, Shieldy or GroupHelp.
---

# Group and channel moderation

## Set up (2 minutes)

1. Open `https://t.me/catalogue_app?start=moderation` (or send `/moderation`).
2. Tap "Pick a group" or "Pick a channel" and choose the chat — Telegram adds
   @catalogue_app as an admin with the rights it needs (delete, restrict, invite,
   pin).
3. A settings panel appears. Turn on what you need:
   - **Service messages: delete** — removes "X joined", "X left", "pinned a
     message", title/photo changes, video chat notices, boosts;
   - **Antiflood** — more than 5 (or 10) messages in 10 seconds → 10-minute mute;
   - **Links**, **Swearing**, **Forwards** — delete and warn;
   - **Stop words** — your own list, comma-separated;
   - **Bots by members: kick** — bots added by non-admins are removed;
   - **Welcome** — greeting for newcomers, `{name}` is replaced with their name;
   - **Rules** — shown by `/rules` and before the captcha.
4. Captcha for join requests: in the chat settings turn on **Approve new
   members** (join requests) and choose @catalogue_app as the bot that checks
   requests. Each applicant solves a picture, letters or your own quiz in a mini
   app; bots don't get in. Options: Premium-only, block very new accounts.

Warnings: 3 warnings → mute for a day. They persist.

## Admin commands (reply to a message)

| Command | Does |
|---|---|
| `/ban`, `/unban` | ban / unban the author |
| `/kick` | remove, can rejoin |
| `/mute 30m`, `/mute 2h`, `/mute 1d`, `/unmute` | mute for a time |
| `/warn`, `/warns`, `/unwarn` | warn, show count, reset |
| `/del` | delete that message |
| `/purge` | delete everything from that message to the command (up to 300) |
| `/pin` (`/pin silent`), `/unpin` | pin / unpin |
| `/rules` | anyone: show the rules |

Service replies of the bot disappear after a minute.

## Channels

In a channel the bot removes service posts ("pinned a message", photo or title
changes, live stream notices) when "Service messages: delete" is on, and can
run the captcha for join requests of a private channel.

## Native Telegram options worth knowing

- Group → Edit → Permissions: slow mode, what members may send.
- Since August 2026 groups and channels have native welcome messages
  (Edit → Welcome Message).

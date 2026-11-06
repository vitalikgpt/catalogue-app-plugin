---
name: telegram-group-moderation
description: Moderate a Telegram group or channel for free with @catalogue_app — delete service messages ("joined", "left", "pinned"), captcha for join requests or right in the chat, antiraid, antiflood, AI antispam for newcomers, filters for links, swearing, forwards and stop words, spam posted as channels, locks for media/stickers/polls/voice, night mode, quiet warnings only the offender sees, /report to admins, a moderation log channel, a shared ban list across your chats, forum topics, and admin commands /ban /mute /warn /kick /del /purge /pin. Use when the user asks for a Telegram moderation bot, antispam, how to remove join/leave messages, a captcha bot, or an alternative to Rose, Combot, Shieldy or GroupHelp.
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

Second page of the panel (⚙️ More):

- **In-chat captcha** — for public groups without join requests: a newcomer is
  muted until they tap the right icon within 3 minutes, otherwise kicked;
- **Antiraid** — 10+ joins a minute: newcomers get a 30-minute mute for 15
  minutes, the owner is alerted;
- **Quiet warnings** — warnings only the offender sees (ephemeral messages);
- **AI antispam** — checks messages of newcomers' first day and of channels
  posting in the chat; spam is deleted and the author muted;
- **Locks** — media, stickers & GIFs, voice and video messages, polls, link
  previews;
- **Night mode** — e.g. "23-7 +3": only admins can write at night, the chat
  reopens in the morning with the previous permissions;
- **Log** — in the group an admin sends `/logto @channel`; bans, mutes,
  warnings, reports and raids are written there.

Messages posted **as a channel** go through the same filters; `/ban` on them
bans the channel. Anonymous admins and the linked channel are trusted.

Warnings: 3 warnings → mute for a day (a channel → banned). They persist.

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
| `/fban`, `/unfban` | ban / unban in **all** your chats connected to the bot |
| `/close`, `/open` | inside a forum topic: close / reopen it |
| `/logto @channel`, `/logto off` | moderation log channel |
| `/rules` | anyone: show the rules |
| `/report` | anyone: reply to a message to alert the admins |

Service replies of the bot disappear after a minute.

## Channels

In a channel the bot removes service posts ("pinned a message", photo or title
changes, live stream notices) when "Service messages: delete" is on, and can
run the captcha for join requests of a private channel.

## Native Telegram options worth knowing

- Group → Edit → Permissions: slow mode, what members may send.
- Since August 2026 groups and channels have native welcome messages
  (Edit → Welcome Message).

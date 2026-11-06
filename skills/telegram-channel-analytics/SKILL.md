---
name: telegram-channel-analytics
description: Telegram channel and group statistics — subscribers and their growth chart, joins and leaves, views and reactions on recent posts, messages and active members in a group. Use when the user asks for Telegram channel analytics, "статистика телеграм канала", subscriber growth, reach, or activity in their chat.
---

# Channel and group analytics

## The user's own channel or group — @catalogue_app

1. Open `https://t.me/catalogue_app?start=stats` (or send `/stats`).
2. Pick the channel or group with the button, forward a post from it, or send
   its `@username`.
3. If asked, add @catalogue_app as an admin — the bot shows a one-tap
   "add as admin" button. Only an admin of that chat can see its analytics.

What it shows:

- subscribers or members now, and a 30-day and 7-day growth chart;
- joined and left;
- for a public channel: number of posts, views and reactions of recent posts;
- for a group: messages and active members over 7 days.

Counting of joins, leaves and messages starts when the bot becomes an admin.
Channels with 500+ subscribers can get language and traffic-source breakdowns
when the stats account suggested by the bot is also added as an admin.

## Any public channel — quick look

`search_channels` (MCP server `catalogue-app`) returns the latest subscriber
count for public channels, chats and bots, and a link to the channel's page on
gramnews.org with its history where available.

## Telegram's own statistics

Channels with enough subscribers have built-in statistics: open the channel →
the ⋮ / profile menu → Statistics. Available to admins only.

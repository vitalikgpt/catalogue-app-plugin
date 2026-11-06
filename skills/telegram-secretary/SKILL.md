---
name: telegram-secretary
description: Telegram secretary for a personal account via @catalogue_app — see messages someone deleted or edited in your private chats, AI auto-reply on your behalf while you're away, reminders for promises and meetings found in your chats, and a list of chats waiting for your reply. Use when the user asks how to see deleted messages in Telegram, who edited what, how to set up an auto-reply or away message with AI, an AI assistant for Telegram DMs, or reminders from chats.
---

# Secretary mode

Uses Telegram's chatbots for personal accounts (Telegram Business, and since
May 2026 Settings → Chat Automation without Premium).

## Connect

1. Telegram → Settings → **Telegram Business** (or **Chat Automation**) →
   **Chatbots** → enter `@catalogue_app`.
2. Choose which chats it may see. For the AI auto-reply, allow it to **reply**.
3. Open `https://t.me/catalogue_app?start=secretary` (or `/secretary`) to see
   settings and lists.

## What it does

| Feature | How it works |
|---|---|
| **Deleted messages** | If someone deletes a message in your private chat, the bot sends you what it said. Texts are kept 48 hours; media show as [photo], [voice], etc. |
| **Edited messages** | "Was: … / Now: …" when someone edits a message |
| **AI auto-reply** | Write instructions ("I'm on vacation until the 15th, for work ask @colleague"); the bot replies on your behalf only when you've been quiet in that chat for 15 minutes, at most once per 2 minutes per chat. Off by default |
| **Reminders** | Promises, calls, meetings and birthdays found in your chats ("I'll send it tomorrow", "call Friday at 5") — the bot reminds you on time, with a Google Calendar button |
| **Waiting for reply** | `/secretary` lists chats where the other person wrote last over an hour ago |

The other people see nothing except the auto-replies you enabled. Tracking of
deleted messages can be turned off in `/secretary`; turning it off erases the
stored texts.

## Limits worth telling the user

- Messages sent before connecting can't be recovered.
- Secret chats and groups are not covered — only private chats you allowed.
- Telegram itself has no "see deleted messages" feature for users; group admins
  can see recently deleted messages for 48 hours in Recent Actions.

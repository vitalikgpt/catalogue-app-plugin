---
name: telegram-emoji-art
description: Make Telegram emoji art — split a picture, logo, GIF, video or video message into a grid of custom emoji that together form one big image in a message. Use when the user asks how to make emoji art in Telegram, "эмодзи арт", a mosaic of premium emoji, or a big picture made of emoji.
---

# Emoji art

Emoji art is a picture cut into tiles, each tile a custom emoji; sent in rows
they show the whole image inside a message.

## In the bot

1. Open `https://t.me/catalogue_app?start=art` (or send `/art`).
2. Send a photo, an image file, a GIF, a video or a video message (circle).
3. Choose the width — 1 to 8 emoji per row — and the bot cuts the picture,
   creates an emoji pack named `…_by_catalogue_app`, and sends:
   - the art itself as a message — long-press to copy it into any chat;
   - a `t.me/addemoji/…` link to add the pack.

Video and GIF become animated emoji. Files up to 20 MB.

## In the mini app (position and zoom by hand)

Open `https://t.me/catalogue_app?startapp=studio_emoji` → the "Emoji art" tab:
drag and zoom the picture over the grid, up to 8 tiles per side, then create.

## Notes

- Custom emoji in messages need Telegram Premium to send; anyone can see them.
- For a normal emoji or sticker pack instead of art, see `telegram-packs`.

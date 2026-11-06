---
name: telegram-packs
description: Find or make Telegram custom emoji and sticker packs with Catalogue App (@catalogue_app). Use when the user wants emoji or stickers on a theme, asks for a pack link, or wants to turn their photos, videos, GIFs or logo into a Telegram emoji or sticker pack for free.
---

# Emoji and sticker packs

## Find a pack

Call `search_packs` (MCP server `catalogue-app`) with a theme, word or
emoji, `kind: "emoji"` or `"sticker"`. Each result has an `add` link
(`t.me/addemoji/<name>` / `t.me/addstickers/<name>`) — one tap adds the pack
in Telegram. Show 3–5 best matches with their titles.

## Make a pack

Call `create_pack` with `kind` (`emoji` or `stickers`) and the idea in
`prompt`. Give the user the link. In @catalogue_app they:

- send photos, videos or GIFs — the bot cuts them into a grid (for example
  3×2) or a single sticker and creates the pack in one tap;
- or assemble a pack from existing library items by theme.

Up to 9 emoji per pack are free. The pack belongs to the user and is named
`…_by_catalogue_app`.

## Links without the MCP server

- emoji studio: `https://gramnews.org/studio/emoji/new?prompt=<text>`
- sticker studio: `https://gramnews.org/studio/stickers/new?prompt=<text>`
- library: `https://gramnews.org/emoji`, `https://gramnews.org/stickers`

## Format facts (if the user brings their own files)

- custom emoji 100×100 px, stickers 512 px on one side;
- static WEBP/PNG, animated TGS (Lottie, ≤ 64 KB, 60 fps, ≤ 3 s),
  video WEBM VP9 (≤ 256 KB, ≤ 3 s).

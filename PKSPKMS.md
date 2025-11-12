---
tags:
  - Backend
  - Personal_Knowledge_Management
  - PKSPKMS
  - Programming_Language/Java
status:
  - Active
type:
  - Project
  - Tag_Page
creationDate: 2025-01-19
modifiedDate: 2025-09-26
published: 2025-07-21
access: Public
description: "[PKMS](./PKMS.md) API and command-line utility."
digitalGarden: Bud
tag_page:
  - PKSPKMS
---

> [!info] I've not yet released it, out of shame. Will do in future.

**P**aul **K**enny'**S** **P**ersonal **K**nowledge **M**anagement **S**ystem

A HTTP API server and command-line tool for [personal knowledge management system](./PKMS.md)s consisting of a single directory and with [[Markdown]] (and any other) files.

Export features:

- Wikilinks to Markdown links

Server features:

- Return result as graph

Originally made to complement [[Obsidian]].

My uses:

- API for [PKSPKMS Bookmarks Browser Extension](./PKSPKMS Bookmarks Browser Extension.md)
- Export publicly marked files from my [PKMS](./PKMS.md) to [My Personal Website](./My Personal Website.md)
- Escape plan for [[Obsidian]]

## Server

```sh
# Start server
pkspkms server -port "3000" -directory "/path/to/notes/"
# In another terminal 
curl GET "http://localhost:3000/list/files?tags=Public" | jq .
```

## Command-line

```sh
# Export JSON graph
pkspkms export -directory "" -query "" -output "" -type "graph" -sqlite-db "" -options "wikilinks,backlinks" -depth "2"
# Export Markdown files
pkspkms export -directory "" -query "" -output "" -type "markdown" -sqlite-db "" -options "wikilinks,backlinks,base" -includeLinked "jpg,png"
```

**Note**: `-depth` retrieves files from outside the query. ==**This can leak your information if you're not careful**==.

## Known Issues

- ==Lots==
- Doesn't support single line, comma separated tags

## (WIP) How It Works Internally, Kinda

![[PKSPKMS Process.excalidraw.svg]]

![PKSPKMS how do.excalidraw.svg](./Resources/Drawings/PKSPKMS how do.excalidraw.svg)

## Other Personal Knowledge Management Software

- Just use a GitHub repo - [costinEEST/almanacs](https://github.com/costinEEST/almanacs)
- [mdzk](https://mdzk.app) - an API for your Markdown vault, see [docs](https://mdzk.app/docs). Very similar to what I'm doing here. Hasn't seen very much development in the [last two years](https://github.com/mdzk-rs/mdzk/commits/main/) (07-2025).
- [SiYuan](https://b3log.org/siyuan/en/), [HN discussion](https://news.ycombinator.com/item?id=42512713) - WYSIWYG wiki
- [[Obsidian]]
- [Logseq](https://logseq.com/) - common Obsidian alternative
- [Heptabase](https://heptabase.com/) - pretty slick looking and I like how annotating looks but it's not file/local first
- [TriliumNext Notes](https://github.com/TriliumNext/Notes)
- [SilverBullet](https://silverbullet.md/) - self-hosted single user
- [Dendron](https://www.dendron.so/) - Visual Studio Code extension
- [xwmx/nb](https://github.com/xwmx/nb) - a crazy amount of features in one portable Shell script

### Lists

- [MaggieAppleton/digital-gardeners](https://github.com/MaggieAppleton/digital-gardeners) - I also like Maggie's other works, I'm subscribed to her blog RSS.
- [lyz-code/best-of-digital-gardens](https://github.com/lyz-code/best-of-digital-gardens) - list of digital gardens
- [KasperZutterman/Second-Brain](https://github.com/KasperZutterman/Second-Brain) - list of second brains

## Tasks

See [[PKSPKMS Tasks]].

## Tagged

| filePath | tags | digitalGarden | Status | type |
|---|---|---|---|---|
| [/PKSPKMS Bookmarks Browser Extension.md](./PKSPKMS Bookmarks Browser Extension.md) | #Firefox #Personal_Knowledge_Management #PKSPKMS #Programming_Language/JavaScript #Web_Browser/Extension | Seed |  | [Project] |
| [/PKSPKMS.md](./PKSPKMS.md) | #Backend #Personal_Knowledge_Management #PKSPKMS #Programming_Language/Java | Bud |  | [Project, Tag_Page] |
| [/My Personal Website.md](./My Personal Website.md) | #Blog #Digital_Garden #Neocities #PKSPKMS #Programming_Language/Haskell #Small_Web | Seed |  | [Project] |


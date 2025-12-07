---
tags:
  - Personal_Knowledge_Management
  - PKSPKMS
  - Programming_Language/Java
status:
  - Active
type:
  - Project
creationDate: 2025-01-19
modifiedDate: 2025-12-06
published: 2025-07-21
url: https://github.com/pskenny/pkspkms
access: Public
description: Markdown [PKMS](PKMS.html) API and command-line export utility
digitalGarden: Bud
---

**P**aul **K**enny'**S** **P**ersonal **K**nowledge **M**anagement **S**ystem

A single user HTTP API server and command-line tool for [personal knowledge management system](PKMS.html)s consisting of a single directory with [[Markdown]] files. Made to complement [Obsidian](Obsidian.html).

My uses:

- API for [[PKSPKMS Bookmarks Browser Extension]]
- Export files from my [PKMS](PKMS.html) to [my personal website](My Personal Website.html)
- Escape plan for [Obsidian](Obsidian.html)

Right now it resolves wiklinks and badly transforms Obsidian Base[^1] (with only one function implemented) and turns it into a table. It's very slow and inefficient.

## Server

```sh
# Start server
java -jar pkspkms.jar server --port "9238" --directory "/path/to/notes/"
# In another terminal 
curl GET "http://localhost:9238/list/files" | jq .
```

Endpoints:

```text
/ping
/list/files
/graph
/graph/depth/2
```

## Command-line

```sh
# Export Markdown files
java -jar pkspkms.jar export --directory "/path/to/notes" --query "" --output "/tmp/output" -type "markdown"
```

## Known Issues

- ==Lots==
- Doesn't support single line, comma separated tags

## Other Personal Knowledge Management Software

- [mdzk](https://mdzk.app) - an API for your Markdown vault, see [docs](https://mdzk.app/docs). Very similar to what I'm doing here. Hasn't seen very much development in the [last two years](https://github.com/mdzk-rs/mdzk/commits/main/) (07-2025).
- [SiYuan](https://b3log.org/siyuan/en/), [HN discussion](https://news.ycombinator.com/item?id=42512713) - WYSIWYG wiki
- [Obsidian](Obsidian.html)
- [Logseq](https://logseq.com/) - commonly recommended Obsidian alternative
- [Heptabase](https://heptabase.com/) - pretty slick looking and I like how annotating looks but it's not file/local first
- [TriliumNext Notes](https://github.com/TriliumNext/Notes)
- [SilverBullet](https://silverbullet.md/) - self-hosted single user
- [Dendron](https://www.dendron.so/) - Visual Studio Code extension
- [xwmx/nb](https://github.com/xwmx/nb) - a crazy amount of features in one portable Shell script

Also see [[Obsidian#Alternatives]].

## Tasks

See [[PKSPKMS Tasks]].

[^1]: It transforms Obsidian Base syntax into [LuaBase](LuaBase.html) and then runs the expressions.

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
modifiedDate: 2025-09-21
published: 2025-07-21
access: Public
digitalGarden: Bud
tag_page:
  - PKSPKMS
---

> [!info] I've not yet released it, out of shame. Will do in future.

**P**aul **K**enny'**S** **P**ersonal **K**nowledge **M**anagement **S**ystem

A HTTP API server and command line tool written in [Java](Java.md) that can get data about Markdown files and their links to each other (and other files) in a directory ([PKMS](PKMS.md)).

Uses YAML frontmatter in Markdown files as metadata and links in text content, including Wikilinks.

Made to complement [Obsidian](Obsidian.md).

My uses:

- API for [PKSPKMS Bookmarks Firefox Extension](PKSPKMS Bookmarks Firefox Extension.md)
- Export files outside of the [PKMS](PKMS.md), like to [My Personal Website](My Personal Website.md)

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

## Features

- Export files
- Export file links graph as JSON
- Bad query language for filtering
- Kinda works a tiny bit with Obsidian Base
- Wikilinks work
- Backlinks
- REST-like API

## Known Issues

- ==Lots==
- Doesn't support single line, comma separated tags

## (WIP) How It Works Internally, Kinda

![PKSPKMS how do.excalidraw.svg](Resources/Drawings/PKSPKMS how do.excalidraw.svg)

## Other Personal Knowledge Management Software

- [mdzk](https://mdzk.app) - an API for your Markdown vault, see [docs](https://mdzk.app/docs). Very similar to what I'm doing here. Hasn't seen very much development in the [last two years](https://github.com/mdzk-rs/mdzk/commits/main/) (07-2025).
- [SiYuan](https://b3log.org/siyuan/en/), [HN discussion](https://news.ycombinator.com/item?id=42512713)
- [Obsidian](Obsidian.md)
- Logseq
- [TheBrain: The Ultimate Digital Memory](https://www.thebrain.com/) - has an interesting way to explore your graph connections
- [Heptabase](https://heptabase.com/) - pretty slick looking and I like how annotating looks but it's not file/local first
- [TriliumNext Notes](https://github.com/TriliumNext/Notes)
- [nb · command line and local web plain text note-taking, bookmarking, archiving, and knowledge base application](https://xwmx.github.io/nb/), [Github](https://xwmx.github.io/nb/)

### Lists

- [MaggieAppleton/digital-gardeners](https://github.com/MaggieAppleton/digital-gardeners) - I also like Maggie's other works, I'm subscribed to her blog RSS.
- [lyz-code/best-of-digital-gardens: Ranked list of awesome digital gardens / second brains](https://github.com/lyz-code/best-of-digital-gardens)
- [KasperZutterman/Second-Brain: list of awesome Public Zettelkastens/Second Brains/Digital Gardens](https://github.com/KasperZutterman/Second-Brain)

## Tasks

<details>
<summary>Tasks</summary>

### TODO

- [ ] Get SQlite DB up and running so it's not hammering your hard drive and taking ages ➕ 2025-06-20
- [ ] Refactor ➕ 2025-07-12

### Potential Features

- [ ] Add [Swagger docs](https://javalin.io/tutorials/openapi-example) ➕ 2025-08-08
- [ ] Add a validation JSON schema endpoint for Markdown YAML ➕ 2025-09-13
- [ ] Watch for file changes and update DB
- [ ] Virtual files?
- [ ] More, better settings
	- [ ] Exclusion list directories
	- [ ] Inclusion list directories
- [ ] Exporting file: have argument to use db file from previous run
- [ ] Use Obsidian settings (point to `.Obsidian` directory?)
- [ ] It'd be cool if when you're exporting a file and a link in that file is for a file that isn't also getting exported it uses that file's `url` property instead of the file in the link when link resolving. Would need multiple file exports though.
</details>

## Tagged

| fileName | tags | digitalGarden |
|---|---|---|
| [PKSPKMS.md](PKSPKMS.md) | [Backend, Personal_Knowledge_Management, PKSPKMS, Programming_Language/Java] | Bud |
| [PKSPKMS Bookmarks Firefox Extension.md](PKSPKMS Bookmarks Firefox Extension.md) | [Firefox, Personal_Knowledge_Management, PKSPKMS, Programming_Language/JavaScript, Web_Browser/Extension] | nil |
| [My Personal Website.md](My Personal Website.md) | [Blog, Digital_Garden, Neocities, PKSPKMS, Programming_Language/Haskell] | Seed |


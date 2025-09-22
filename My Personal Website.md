---
aliases: [My Website]
tags:
  - Blog
  - Digital_Garden
  - Neocities
  - PKSPKMS
  - Programming_Language/Haskell
  - Small_Web
status:
  - Active
type:
  - Project
creationDate: 2025-06-30
modifiedDate: 2025-09-21
published: 2025-08-06
publicUrl: https://paulkenny.neocities.org/
access: Public
digitalGarden: Seed
---

I've turned my private, half-assed [PKMS](PKMS.md) into a public, no-assed [Digital Garden](Digital Garden.md). Hosted on [Neocities](Neocities.md).

![neocitiesbadge.svg](Resources/Image/neocitiesbadge.svg)

It's a [Haskell](Haskell.md) program (written using [Hakyll](Hakyll.md)) that builds the website from a bunch of Markdown and JSON files when executed. I have a script to load the Markdown files and (JSON) graph data from my PKMS using [PKSPKMS](PKSPKMS.md) from my personal notes directory. It's a very long and effortful way to make your own [Obsidian Publish](https://obsidian.md/publish) alternative.

The design is heavily copying the look of [Obsidian](Obsidian.md) since that's my main editor. I'd like to add more graph traversal features in the future though. Maybe. Possibly.

 Here's what it kinda looks like building the website as a graph:

 ![My personal website build.excalidraw.svg](Resources/Drawings/My personal website build.excalidraw.svg)

## Features

- Has a graph of the links to and from the note as well as tags
- RSS (kinda, it needs some love and care)
- No email sign ups

## Resources

- [Network Graphs: Visualizing Relationships and Connections in Research Data](https://editverse.com/network-graphs-visualizing-relationships-in-research-data/)
- You can find the Markdown files this website is generated from in this Git repo: [GitHub - pskenny/notes](https://github.com/pskenny/notes)

## Tasks

<details>
<summary>Tasks</summary>

### Site

- [x] Initial Git commit ➕ 2025-08-20 ✅ 2025-08-25
- [ ] Add Open Graph Metadata to pages ➕ 2025-08-26
- [ ] ==Refactor everything== ➕ 2025-07-12
- [x] Create separate Git repo that only includes Markdown/text files, reflecting content in website ➕ 2025-07-20 ✅ 2025-08-08
- [ ] Check out [pandoc-sidenote](https://github.com/jez/pandoc-sidenote) ➕ 2025-07-14
- [ ] Make 404 page ➕ 2025-07-12
- [ ] Fix `tags.html` (currently empty) ➕ 2025-07-12
- [ ] Add descriptions to RSS ➕ 2025-07-12
- [ ] Add [jampack.](https://github.com/divriots/jampack) to the pipeline ➕ 2025-07-11
- [ ] Add table of content to pages ➕ 2025-07-11
- [x] External links have icon beside them as visual indicator ➕ 2025-07-11
- [ ] Add backlinks to bottom of pages ➕ 2025-07-11
- [x] Copy all Markdown files with Public tag into separate temporary directory using [PKSPKMS](PKSPKMS.md) ✅ 2025-07-10
	- [x] Copy linked resources such as images (requires change in [PKSPKMS](PKSPKMS.md))
- [ ] Try it out on other people's notes (i.e. GitHub repo with an appropriate license) ➕ 2025-07-15

### Graph

- [ ] Make button appear at top of graph when full screen in mobile ➕ 2025-08-20
- [ ] Add ability to filter nodes based on properties ➕ 2025-07-22
- [ ] Toggle switch for graph of depth 1 or 2 ➕ 2025-07-20

### Done

- [x] Make graph resizeable or add a full page size button ➕ 2025-07-20 ✅ 2025-07-22
- [x] Make file graph nodes larger the more edges they have ➕ 2025-07-21 ✅ 2025-07-22
- [x] Add hover over window/frame showing link page ➕ 2025-07-21 ✅ 2025-07-21
- [x] If a page has `publicUrl`, that should be at the top of the page, not hidden in frontmatter ➕ 2025-07-21 ✅ 2025-07-21
- [x] Add graphs ➕ 2025-07-11 ✅ 2025-07-12
	- [x] Default depth 2 graphs for pages ✅ 2025-07-15
- [x] Use [PKSPKMS](PKSPKMS.md) to export files with wikilinks into relative urls ✅ 2025-07-10
- [x] Compile and run [Hakyll](Hakyll.md) site ✅ 2025-07-10
- [x] Delete Markdown files ✅ 2025-07-10
- [x] Add RSS ✅ 2025-07-11
	- [x] Add RSS for tags ✅ 2025-07-11
- [x] Fix resized display bug overflow ➕ 2025-07-11 ✅ 2025-07-12
- [x] Make tag pages hierarchical ➕ 2025-07-12 ✅ 2025-07-20 (no thank you)
</details>

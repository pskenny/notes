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

I've turned my private, half-assed [PKMS](./PKMS.md) into a public, no-assed [Digital Garden](./Digital Garden.md). Hosted on [Neocities](./Neocities.md).

![neocitiesbadge.svg](./Resources/Image/neocitiesbadge.svg)

It's a [[Haskell]] program (written using [Hakyll](./Hakyll.md)) that builds the website from a bunch of Markdown and JSON files when executed. I have a script to load the Markdown files and (JSON) graph data from my PKMS using [PKSPKMS](./PKSPKMS.md) from my personal notes directory. It's a very long and effortful way to make your own [Obsidian Publish](https://obsidian.md/publish) alternative.

The design is heavily copying the look of [[Obsidian]] since that's my main editor. I'd like to add more graph traversal features in the future though. Maybe. Possibly.

 Here's what it kinda looks like building the website as a graph:

 ![My personal website build.excalidraw.svg](./Resources/Drawings/My personal website build.excalidraw.svg)

## Features

- Has a graph of the links to and from the note as well as tags (I think it might be broken (Sept 22, 2025))
- RSS (kinda, it needs some love and care)
	- Every tag gets an RSS feed
- No email sign ups

## Resources

- [Network Graphs: Visualizing Relationships and Connections in Research Data](https://editverse.com/network-graphs-visualizing-relationships-in-research-data/)
- You can find the Markdown files this website is generated from in this Git repo: [GitHub - pskenny/notes](https://github.com/pskenny/notes)

## Tasks

<details>
<summary>Tasks</summary>

### Site

- [ ] Add Open Graph Metadata to pages ➕ 2025-08-26
- [ ] ==Refactor everything== ➕ 2025-07-12
- [ ] Check out [pandoc-sidenote](https://github.com/jez/pandoc-sidenote) ➕ 2025-07-14
- [ ] Make 404 page ➕ 2025-07-12
- [ ] Fix `tags.html` (currently empty) ➕ 2025-07-12
- [ ] Add descriptions to RSS ➕ 2025-07-12
- [ ] Add [jampack](https://github.com/divriots/jampack) to the pipeline ➕ 2025-07-11
- [ ] Add table of content to pages ➕ 2025-07-11
- [ ] Add backlinks to bottom of pages ➕ 2025-07-11
- [ ] Try it out on other people's notes (i.e. GitHub repo with an appropriate license) ➕ 2025-07-15

### Graph

- [ ] Make button appear at top of graph when full screen in mobile ➕ 2025-08-20
- [ ] Add ability to filter nodes based on properties ➕ 2025-07-22
- [ ] Toggle switch for graph of depth 1 or 2 ➕ 2025-07-20

</details>

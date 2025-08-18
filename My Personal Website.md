---
aliases: [My Website]
tags:
  - Blog
  - Digital_Garden
  - PKSPKMS
  - Programming_Language/Haskell
status:
  - Active
type:
  - Project
creationDate: 2025-06-30
modifiedDate: 2025-08-08
published: 2025-08-06
publicUrl: https://paulkenny.neocities.org/
access: Public
---

I've turned my private half-assed PKMS into a public no-assed digital garden.

It's a [Haskell](Haskell.md) program written using [Hakyll](Hakyll.md) that builds the website when executed. I have scripts to load in files and graph data from my [[PKMS]].

The steps are:

- Get public marked files using [PKSPKMS](PKSPKMS.md)
- Sanitise frontmatter
- Export them using PKSPKMS to get rid of nonstandard Markdown (Wikilinks, Dataview queries, etc)
- Build and run program
- Check for dead links using Lychee

Hosted on [Neocities](Neocities.md).

The design is heavily copying the look of [Obsidian](Obsidian.md). I'd like to add more graph traversal features in the future though.

## Todo

### Site

- [ ] ==Refactor everything== ➕ 2025-07-12
- [x] Create separate Git repo that only includes Markdown/text files, reflecting content in website ➕ 2025-07-20 ✅ 2025-08-08
- [ ] Check out [pandoc-sidenote](https://github.com/jez/pandoc-sidenote) ➕ 2025-07-14
- [ ] Make 404 page ➕ 2025-07-12
- [ ] Fix tags page (currently empty) ➕ 2025-07-12
- [ ] Add descriptions to RSS ➕ 2025-07-12
- [ ] Add [jampack.](https://github.com/divriots/jampack) to the pipeline ➕ 2025-07-11
- [ ] Improve `blog.sh` output with colours 🌈 ➕ 2025-07-11
- [ ] Add table of content to pages ➕ 2025-07-11
- [ ] External links have icon beside them as visual indicator ➕ 2025-07-11
- [ ] Add backlinks to bottom of pages ➕ 2025-07-11
- [x] Copy all Markdown files with Public tag into separate temporary directory using [PKSPKMS](PKSPKMS.md) ✅ 2025-07-10
	- [ ] Copy linked resources such as images, requires change in [PKSPKMS](PKSPKMS.md)
- [ ] Try it out on other people's notes ➕ 2025-07-15

### Graph

- [ ] Add ability to filter nodes based on properties ➕ 2025-07-22
- [ ] Toggle switch for graph of depth 1 or 2 ➕ 2025-07-20

### Hover Over

- [ ] Add hover over pinning

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

## Resources

- [tinysearch](https://github.com/tinysearch/tinysearch) full-text search engine for static websites
- [Network Graphs: Visualizing Relationships and Connections in Research Data](https://editverse.com/network-graphs-visualizing-relationships-in-research-data/)

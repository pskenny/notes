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
creationDate: 2025-01-19
modifiedDate: 2025-08-08
published: 2025-07-21
access: Public
---

> [!info] I've not yet released it, out of shame. Will do in future.

**P**aul **K**enny'**S** **P**ersonal **K**nowledge **M**anagement **S**ystem

A HTTP API server and command line tool written in [Java](Java.md) that can get data about Markdown files and their links to each other (and other files) in a directory ([[PKMS]]).

Uses YAML frontmatter in Markdown files as metadata and links in text content, including Wikilinks.

Made to complement [Obsidian](Obsidian.md).

My uses:

- API for [PKSPKMS Bookmarks Firefox Extension](PKSPKMS Bookmarks Firefox Extension.md)
- Export files outside of the [[PKMS]], like to my website

## Server

Currently there is no security for the server. Don't use it.

```sh
# Start server
pkspkms server -port "3000" -directory ""
# In another terminal 
curl GET "http://localhost:3000/list/files?tags=Public" | jq .
```

Will return something like:

```json
{
	files: [
		{
		
		}
	]
}
```

## Command-line

```sh
# Export JSON graph
pkspkms export -directory "" -query "" -output "" -type "graph" -sqlite-db "" -options "wikilinks,backlinks" -depth "2"
# Export Markdown files
pkspkms export -directory "" -query "" -output "" -type "markdown" -sqlite-db "" -options "wikilinks,backlinks" -includeLinked "jpg,png"
```

**Note**: `-depth` retrieves files from outside the query. This can leak you information if you're not careful.

## TODO

- [ ] Get SQlite DB up and running so it's not hammering your hard drive and taking ages ➕ 2025-06-20
- [ ] Refractor ➕ 2025-07-12
- [ ] Use [docopt](docopt.md) format for CLI ➕ 2025-07-17
- [ ] Add [Swagger docs](https://javalin.io/tutorials/openapi-example) ➕ 2025-08-08

## Potential Features

- [ ] Watch for file changes and update DB
- [ ] Virtual files
- [ ] More, better server settings
	- [ ] Exclusion list directories
	- [ ] Inclusion list directories
- [ ] Export file
	- [ ] Have argument to use db file from previous run
	- [ ] Markdown
		- [ ] Replace Wikilinks with relative markdown links
	- [ ] Graph
		- Export JSON with links, backlinks and tags
	- [ ] HTML
	- [ ] Plaintext
- [ ] Use Obsidian settings (point to `.Obsidian` directory?)
- [ ] It'd be cool if when you're exporting a file and a link in that file is for a file that isn't also getting exported it uses that file's `url` property instead of the file in the link when link resolving. Would need multiple file exports though.
- [ ] Could abuse Markdown comments for my own dynamic syntax: [syntax - Comments in Markdown - Stack Overflow](https://stackoverflow.com/questions/4823468/comments-in-markdown)
- [ ] Export rules as JSON (`pkspkms export -json ''`):

```json
{
	"export": [
		{
			"query": 'tags=Blog*',
			"type": "markdown",
			"steps": ["wikilinkToRelativeLink", "bringLocallyLinked"],
			"destination": "/blog/posts/"
		}
	]
}
```

## Known Issues

- Lots
- Doesn't support single line, comma separated tags

## Other Personal Knowledge Management Software, Solutions, Etc

- [mdzk](https://mdzk.app) - an API for your Markdown vault, see [docs](https://mdzk.app/docs)￼. Very similar to what I'm doing here. Hasn't seen very much development in the last two years (07-2025).
- [SiYuan](https://b3log.org/siyuan/en/), [HN discussion](https://news.ycombinator.com/item?id=42512713)
- [Obsidian](Obsidian.md)
- Logseq
- [TheBrain: The Ultimate Digital Memory](https://www.thebrain.com/) - has an interesting way to explore your graph connections
- [Heptabase](https://heptabase.com/) - pretty slick looking and I like how annotating looks but it's not file first
- [TriliumNext Notes](https://github.com/TriliumNext/Notes)
- [nb · command line and local web plain text note-taking, bookmarking, archiving, and knowledge base application](https://xwmx.github.io/nb/), [Github](https://xwmx.github.io/nb/)

### Lists

- [GitHub - MaggieAppleton/digital-gardeners: Resources, links, projects, and ideas for gardeners tending their digital notes on the public interwebs](https://github.com/MaggieAppleton/digital-gardeners) - I also like Maggie's other works, I'm subscribed to her blogs RSS
- [GitHub - lyz-code/best-of-digital-gardens: Ranked list of awesome digital gardens / second brains](https://github.com/lyz-code/best-of-digital-gardens)
- [GitHub - KasperZutterman/Second-Brain: A curated list of awesome Public Zettelkastens 🗄️ / Second Brains 🧠 / Digital Gardens 🌱](https://github.com/KasperZutterman/Second-Brain)

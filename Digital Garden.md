---
tags:
  - Digital_Garden
  - Meta
  - Personal_Knowledge_Management
  - Terminology
type:
  - Tag_Page
creationDate: 2025-06-01
modifiedDate: 2025-09-20
published: 2025-07-01
access: Public
digitalGarden: Seed
tag_page:
  - Digital_Garden
---

A Digital Garden is a computer-y cultivated space for knowledge. Adding, editing, removing, and restructuring informal (sometimes *very* loose) information. Emphasise the connections between things. Rinse and repeat. You can do it without touching any code too. It can be totally private. Mine is mostly private.

![digital garden.excalidraw.svg](Resources/Drawings/digital garden.excalidraw.svg)

I've three categories:

- **Seed** - new, small, not built upon.
- **Bud** - rough, a bit more expanded upon and effort expended.
- **Evergreen** - all good, nothing more needed or it's been expanded upon enough.

## Catalogue

### Seeds

```base
views:
  - type: table
    name: Table
    filters:
      and:
        - digitalGarden == "Seed"
    order:
      - file.name
      - file.tags
      - creationDate
      - modifiedDate
      - access
    sort:
      - property: access
        direction: DESC
      - property: file.name
        direction: ASC
    columnSize:
      file.tags: 360
      note.creationDate: 200

```

### Budding

| fileName | tags |
|---|---|
| [just serendipity.md](just serendipity.md) | [Blog, Tech] |
| [PKSPKMS.md](PKSPKMS.md) | [Backend, Personal_Knowledge_Management, PKSPKMS, Programming_Language/Java] |
| [Podcasts I Like.md](Podcasts I Like.md) | [I_Like, List, Podcast] |
| [Blogs I Like.md](Blogs I Like.md) | [Blog, I_Like, List] |
| [Programs I Like.md](Programs I Like.md) | [Android, App, I_Like, Linux, List, Program] |


## Evergreen

| fileName | tags | type |
|---|---|---|
| [The Zen Of Python.md](The Zen Of Python.md) | [Advice, Programming_Language/Python, Software_Development] | [Blog/Quote] |
| [YTCH.md](YTCH.md) | [Best_Of/2024, Entertainment, Video, YouTube] | [Blog/Link, Bookmark] |
| [==ESPY.WORLD==.md](==ESPY.WORLD==.md) | [Art, Comic, Trinket/Website] | [Blog/Link, Bookmark] |
| [A rant on personal engineering projects.md](A rant on personal engineering projects.md) | [Best_Of/2024, Project_Management, Video] | [Blog/Link, Bookmark] |
| [WTFPL.md](WTFPL.md) | [Legal, Software_License] | nil |
| [Things I Liked And Learned 2020.md](Things I Liked And Learned 2020.md) | [Things_I_Liked_And_Learned] | [Blog/Post] |
| [Things I Liked And Learned 2021.md](Things I Liked And Learned 2021.md) | [Things_I_Liked_And_Learned] | [Blog/Post] |
| [time HTML element.md](time HTML element.md) | [HTML, TIL] | nil |
| [Fullscreen Java Terminal Windows.md](Fullscreen Java Terminal Windows.md) | [Code_Snippet, Commandline, Programming_Language/Java, Terminal, TUI] | [Blog/Post] |


## Links

- [🌱 My blog is a digital garden, not a blog](https://joelhooks.com/digital-garden)
- [How to set up your own digital garden](https://nesslabs.com/digital-garden-set-up)
- [Externalism Wikipedia entry](https://en.wikipedia.org/wiki/Externalism)

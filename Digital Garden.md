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
- **Evergreen** - all good, nothing more needed or it's been expanded upon enough. Also see [Evergreen notes](https://notes.andymatuschak.org/z5E5QawiXCMbtNtupvxeoEX).

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
| [just serendipity.md](just serendipity.md) | [Blog](/tags/Blog.html), [Tech](/tags/Tech.html) |
| [PKSPKMS.md](PKSPKMS.md) | [Backend](/tags/Backend.html), [Personal_Knowledge_Management](/tags/Personal_Knowledge_Management.html), [PKSPKMS](/tags/PKSPKMS.html), [Programming_Language/Java](/tags/Programming_Language/Java.html) |
| [Podcasts I Like.md](Podcasts I Like.md) | [I_Like](/tags/I_Like.html), [List](/tags/List.html), [Podcast](/tags/Podcast.html) |
| [Blogs I Like.md](Blogs I Like.md) | [Blog](/tags/Blog.html), [I_Like](/tags/I_Like.html), [List](/tags/List.html) |
| [Programs I Like.md](Programs I Like.md) | [Android](/tags/Android.html), [App](/tags/App.html), [I_Like](/tags/I_Like.html), [Linux](/tags/Linux.html), [List](/tags/List.html), [Program](/tags/Program.html) |


## Evergreen

| fileName | tags | type |
|---|---|---|
| [The Zen Of Python.md](The Zen Of Python.md) | [Advice](/tags/Advice.html), [Programming_Language/Python](/tags/Programming_Language/Python.html), [Software_Development](/tags/Software_Development.html) | [Blog/Quote] |
| [YTCH.md](YTCH.md) | [Best_Of/2024](/tags/Best_Of/2024.html), [Entertainment](/tags/Entertainment.html), [Video](/tags/Video.html), [YouTube](/tags/YouTube.html) | [Blog/Link, Bookmark] |
| [==ESPY.WORLD==.md](==ESPY.WORLD==.md) | [Art](/tags/Art.html), [Comic](/tags/Comic.html), [Trinket/Website](/tags/Trinket/Website.html) | [Blog/Link, Bookmark] |
| [A rant on personal engineering projects.md](A rant on personal engineering projects.md) | [Best_Of/2024](/tags/Best_Of/2024.html), [Project_Management](/tags/Project_Management.html), [Video](/tags/Video.html) | [Blog/Link, Bookmark] |
| [WTFPL.md](WTFPL.md) | [Legal](/tags/Legal.html), [Software_License](/tags/Software_License.html) | nil |
| [Things I Liked And Learned 2020.md](Things I Liked And Learned 2020.md) | [Things_I_Liked_And_Learned](/tags/Things_I_Liked_And_Learned.html) | [Blog/Post] |
| [Things I Liked And Learned 2021.md](Things I Liked And Learned 2021.md) | [Things_I_Liked_And_Learned](/tags/Things_I_Liked_And_Learned.html) | [Blog/Post] |
| [time HTML element.md](time HTML element.md) | [HTML](/tags/HTML.html), [TIL](/tags/TIL.html) | nil |
| [Fullscreen Java Terminal Windows.md](Fullscreen Java Terminal Windows.md) | [Code_Snippet](/tags/Code_Snippet.html), [Commandline](/tags/Commandline.html), [Programming_Language/Java](/tags/Programming_Language/Java.html), [Terminal](/tags/Terminal.html), [TUI](/tags/TUI.html) | [Blog/Post] |


## Links

- [🌱 My blog is a digital garden, not a blog](https://joelhooks.com/digital-garden)
- [How to set up your own digital garden](https://nesslabs.com/digital-garden-set-up)
- [Externalism Wikipedia entry](https://en.wikipedia.org/wiki/Externalism)

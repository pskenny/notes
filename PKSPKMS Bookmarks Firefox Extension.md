---
tags:
  - Firefox
  - Personal_Knowledge_Management
  - PKSPKMS
  - Programming_Language/JavaScript
  - Web_Browser/Extension
status:
  - Inactive
type:
  - Project
creationDate: 2024-10-01
modifiedDate: 2025-09-08
published: 2025-07-01
publicUrl: https://github.com/pskenny/pkspkms-bookmarks-extension
access: Public
digitalGarden: Seed
---

 > [!info] This has not yet been release, out of shame. I will do it someday.

A Firefox extension using [PKSPKMS](PKSPKMS.md) to use local Markdown files as bookmarks.

Inspired to make this after reading [The best browser bookmarking system is already built-in](https://afewthingz.com/browserbookmark) ([HN](https://news.ycombinator.com/item?id=41696560)).

Minimal bookmark Markdown file:

```markdown
---
tags: Bookmark
publicUrl:
---
```

Multiple `Bookmark` tags put the same link in multiple folders.

## TODO

- [ ] Fix folders not expanding on child expands
- [ ] Close popup when link clicked
- [ ] Make a distributable
- [ ] Install it
- [ ] Set up PKSPKSMS to run on startup

### Potential Additional Tasks

- [ ] Check if the current tab is bookmarked already (search by URL field) ➕ 2025-09-08
- [x] Add search functionality ✅ 2025-07-11
	- [ ] Add bookmark search functionality
	- [ ] Add history search functionality
- [ ] Publish on addons store
- [ ] Include first line or property value from Markdown file as bookmark subtitle.
- [ ] Display tags underneath Bookmark link
	- [ ] Clickable tags

### Development Resources

- [Getting started with web-ext | Firefox Extension Workshop](https://extensionworkshop.com/documentation/develop/getting-started-with-web-ext/)
- [Obsidian URI - Obsidian Help](https://help.obsidian.md/Extending+Obsidian/Obsidian+URI)

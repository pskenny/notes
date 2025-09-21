---
tags:
  - Networking
  - Project_Gemini
type:
  - Bookmark
creationDate: 2025-08-08
modifiedDate: 2025-08-08
published: 2025-08-09
publicUrl: https://geminiprotocol.net/docs/specification.gmi
access: Public
bookmark:
  - Computing
digitalGarden: Seed
---

A network protocol and hypertext format. Initial release was 2019.

> Gemini is a new internet technology supporting an electronic library of interconnected text documents. That's not a new idea, but it's not old fashioned either. It's timeless, and deserves tools which treat it as a first class concept, not a vestigial corner case. Gemini isn't about innovation or disruption, it's about providing some respite for those who feel the internet has been disrupted enough already. We're not out to change the world or destroy other technologies. We are out to build a lightweight online space where documents are just documents, in the interests of every reader's privacy, attention and bandwidth.
>
> - *[Project Gemini](https://geminiprotocol.net/)*

## Network Protocol

> …This document specifies the Gemini protocol for file transfer. It can be thought of as an incremental improvement over Gopher [RFC1436] rather than a stripped down HTTP [RFC7230]. It runs over TCP [STD7] port 1965 with encryption provided by TLS [RFC8446] with a simple request and response transaction….
>
> - *Gemini network protocol specification, Abstract, Version 0.24.1*

## Hypertext Format

The hypertext format is heavily inspired by Markdown and the style of the content is almost entirely decided on the end device, not in the page.

Gemini links begin with `gemini://` (in contrast to `http://`).

## Resources

- [gopher:// The web before the web (by RetroBytes) - YouTube](https://www.youtube.com/watch?v=b4aApVkvrNU)
- [Lagrange](https://gmi.skyjake.fi/lagrange/) - Desktop Gemini client (think something Firefox or Chrome but for Gemini)

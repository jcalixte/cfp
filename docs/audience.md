# Audience & takeaways

## Why this talk, why now

- **It's a real, working system — and an honest one.** Everything runs in production, and I'm the first user: **52 notes already published** from my own repo — bilingual, spanning software craft, Lean/TPS, systems thinking, society, and Japanese aesthetics — through the `remanso-cli` publish path, the `site.standard.document` and `space.remanso.note` lexicons, an OAuth client, and a self‑hosted Jetstream AppView. Remanso isn't finished, and I'll say what's still rough.
- **It reframes "own your data" as something you'd actually do.** Everyone nods at data ownership; nobody acts on it. Tying it to a habit people already have — note‑taking — makes the payoff tangible: *the notes you already write can become a blog you own, today.*
- **It's the missing kind of atproto talk.** Most explain Bluesky‑the‑app. Very few show an *independent developer* shipping a non‑microblog product on the protocol — which is exactly where the interesting design questions live (custom lexicons, AppViews, reusing the graph).
- **The timing is right.** The atproto blogging ecosystem just became real — shared lexicons (`standard.site`), community tools (Sequoia), explorers (pdsls, lexicon.garden). It's past "what is it" and into "what can I build."

## Key takeaways

The audience will leave able to:

1. **Internalize `File > Protocol > App`** as a way to choose tools that won't trap their work.
2. **Explain what the AT Protocol is** underneath Bluesky — identity, PDS, lexicons, firehose — as a *social filesystem*, without hand‑waving.
3. **See data ownership made concrete**: records on a server you control, addressed by your identity, readable by any app.
4. **Choose between a custom and a shared lexicon**, and understand the interop trade‑off.
5. **Reuse an existing social graph** instead of bootstrapping an audience from zero.
6. **Sketch a minimal AppView** (firehose → store → API) they could build themselves.

## Target audience & level

- **Who**: web/indie developers, digital‑gardeners, the "I have a notes folder and a half‑dead blog" crowd, and anyone curious about decentralized social beyond "Bluesky is Twitter again."
- **Level**: intermediate. Comfortable with web fundamentals (HTTP, JSON, OAuth at a glance). **No prior AT Protocol knowledge required** — the concepts section is self‑contained.
- **Not required**: experience with Bluesky, federation, or distributed systems.

# Talk outline & format

## Detailed outline *(designed for a 25–30 min slot; timings approximate)*

1. **The child in the room** *(≈4 min)*
   - Why I started: not to publish, but to stop being the one who couldn't counter an argument.
   - 2021 → today: permanent notes, backlinks, stacked reading; 800+ notes; *my voice counted*.
   - The closed door: a private garden in a Git repo is durable and mine — and invisible.

2. **`File > Protocol > App`** *(≈4 min)* — the spine of the talk:
   - **File over app** (Ango): own durable files, not app silos.
   - **A social filesystem** (Abramov): a protocol turns those files into a *shared, social* filesystem.
   - **Apps killed the links**: why platforms keep you in and the open web pushes you out — and why the ordering matters.

3. **AT Protocol in five minutes** *(≈6 min)* — the only "concepts" section, framed as a filesystem:
   - **Identity** = a portable name (DID / handle) you keep across apps.
   - **PDS** = your personal repository — the filesystem you own.
   - **Lexicons** = typed schemas (file types); anyone can define one (`space.remanso.note` is mine).
   - **Firehose / Jetstream + AppViews** = the stream of changes, and how apps read the network without a central database.

4. **Opening the garage door — Remanso** *(≈11 min)* — live, on screen:
   - **Publish in one gesture**: `*.pub.md` + commit → `remanso publish` (a CLI I forked from the community's Sequoia, run locally or as a GitHub Action) → records on my PDS, with content‑hash change detection and the resulting `atUri` written back into the note's frontmatter. *Lower every wall.*
   - **Lexicons — reach vs. richness**: my 52 notes are published as *shared* `site.standard.document` records, so my static blog at apoena.dev — and any other `standard.site` reader — renders them for free. The toolchain also supports a richer custom lexicon, `space.remanso.note` (LaTeX, Mermaid, embeds, image blobs, language, theme), for the Remanso client. Interop **and** custom power.
   - **Read with someone else's graph**: build a "following" feed from `app.bsky.graph.getFollows` — I inherited a social network instead of begging people to join one.
   - **Auth without secrets, identity you can prove**: a browser OAuth client (DPoP‑bound tokens, public `client-metadata.json`, no client secret) for in‑app publishing — and `remanso inject` drops verification link tags into the static site, so the writing is provably tied to my atproto identity.
   - **Your own AppView**: a Deno Jetstream consumer filtering my collection into SQLite, served as a tiny REST API, self‑hosted on my own infra (Coolify + Gitea).

5. **What this changes — and what it doesn't** *(≈4 min)*
   - Takeaways, and an honest list of rough edges (lexicon design, blob limits, discovery, "it's still early").
   - The blueprint: how *you* could publish your notes this week. *Learn, Think, Write, Share.*

> **Lightning‑talk variant (5–10 min):** keep sections 1, 2, and the *publish‑in‑one‑gesture* + *borrow‑the‑graph* beats of section 4. Drop the deep concepts and the AppView internals.

## Format & logistics

- **Preferred length**: 25–30 min + Q&A. Compresses cleanly to a 5–10 min lightning talk (see variant above).
- **Style**: narrative — a personal story carrying a technical spine — with live walk‑throughs of real code and real published records (no slideware‑only abstractions).
- **A/V**: standard projector/HDMI; I run the demo from my own laptop. Internet is *nice‑to‑have* (live publish demo) but I'll have a recorded fallback so the talk survives venue Wi‑Fi.
- **Language**: English (also available in French).

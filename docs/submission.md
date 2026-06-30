# Submission kit

## Speaker bio *(fill in / trim to the venue's word limit)*

Julien Calixte — *[role / company]*. Indie developer who builds and self‑hosts small web apps on his own infrastructure (the `*.apoena.dev` stack). A five‑years‑deep note‑taker and recent convert to publishing in the open, he built **Remanso** (grown out of his private "Lite Note" habit) to put his writing on the AT Protocol under one motto: *Learn, Think, Write, Share.*

- Blog: https://apoena.dev
- Project: https://remanso.space
- *[Bluesky handle, GitHub, etc. — add]*

## Supporting material *(for reviewers)*

- **My journey, in my own words** (published on atproto via Remanso): *"My journey in the AT Proto world"*, *"Apps killed the links"*, *"Personal websites are the new web."*
- **The published corpus**: 52 `*.pub.md` notes live on my PDS (`did:plc:4m3kouplb7s7xozjd3whinvl`, collection `site.standard.document`) — browsable on [pdsls.dev](https://pdsls.dev/at://did:plc:4m3kouplb7s7xozjd3whinvl/site.standard.document). Range: software craft (SRP, microcommits, code calisthenics), Lean/TPS (jidoka, gemba, poka‑yoke, takt time), systems thinking (Meadows' traps), society & politics, philosophy, and Japanese aesthetics (Ma 間, Sakura 桜, Takumi 匠).
- **Remanso** (the publishing client + custom lexicon): https://remanso.space — lexicon `space.remanso.note` (see it in the wild on [ufos.microcosm.blue](https://ufos.microcosm.blue/collection/?nsid=space.remanso.note)).
- **`remanso-cli`**: the publishing engine — a Bun/TypeScript CLI (`auth` / `init` / `publish` / `sync` / `inject`) that writes `*.pub.md` notes to a PDS as *both* `space.remanso.note` and `site.standard.document` records, run locally or as a GitHub Action. A fork of the community's [Sequoia](https://sequoia.pub) by Steve Dylan, extended to emit the custom Remanso lexicon.
- **The AppView** (`remanso-jetstream`): a Deno Jetstream consumer for `space.remanso.note` → SQLite → REST.
- **apoena.dev**: a static blog (îles) that renders `site.standard.document` records read from a PDS at build time — proof of the interop angle.
- **The essays**: [File over app](https://stephango.com/file-over-app) · [A social filesystem](https://overreacted.io/a-social-filesystem/).

## Tailoring checklist

A CFP lands best when it's aimed. Before submitting to a specific conference, fill these in — they're the things only you can decide:

- [ ] **Target conference / track** — and trim each section to its stated word limits (short vs. detailed abstract are usually separate fields).
- [ ] **Exact talk length** offered by the CFP (the outline assumes 25–30 min; pick the variant).
- [ ] **How personal / political to go.** The "child in the room" origin and the Bluesky‑as‑refuge motivation are what make this talk *yours* and not a generic atproto intro — I'd keep a measured version. But how far to foreground the values angle depends on the venue; dial it to the audience.
- [ ] **Lead with your real numbers** — **5 years, 800+ private notes, 52 published** (bilingual, across Lean/TPS, systems thinking, software craft, society, philosophy, Japanese aesthetics). Add "self‑hosted on €X/mo" if you want a cost angle. These are all real — use them.
- [ ] **The diagram.** Your journey note literally says *"I need a diagram"* (the personal site ↔ Remanso ↔ Leaflet ↔ PDS picture). Worth drawing for the talk and maybe the proposal.
- [ ] **Speaker bio** specifics (role, company, Bluesky handle, prior speaking).
- [ ] **Credit colas.dev** for the ops/infra on stage if appropriate.
- [ ] **Confirm what's demoable live** vs. recorded, so the abstract doesn't promise more than the Wi‑Fi can deliver.

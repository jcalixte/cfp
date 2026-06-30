# CFP — `File > Protocol > App`: How a Note‑Taking Habit Became a Voice I Own

> A conference talk proposal by **Julien Calixte**. Working draft.

For years I was *the child in the room* — agreeing with everyone, able to counter no one. So I started taking notes, and slowly my voice counted. This is the story of how a 5‑year, 800‑note private garden became a public voice I own — **52 notes and counting**, published to the AT Protocol instead of a platform.

## Abstract

We all keep notes; far fewer publish them — because going public usually means renting your voice from a platform that owns your content, your identity, and your audience. I'll tell the story of turning a five‑year, 800‑note habit into a public blog I own, on the AT Protocol. The thesis is a hierarchy: **`File > Protocol > App`**. Your files outlive apps (Steph Ango); a protocol turns them into a *social filesystem* (Dan Abramov); the app is just a lens.

## Architecture

One source of truth (your files), one network you own (the protocol), many lenses to read it (the apps).

```text
        FILE  ───▶  PROTOCOL  ───▶  APP
       (own it)    (share it)      (read it — many lenses, one source)


   ┌──────────────────────────────┐
   │ FILE — your notes            │
   │ Markdown in a Git repo       │
   │ Zettelkasten: notes + links  │
   │   note.md                    │
   │   note.pub.md   ◀── publish  │
   └───────────────┬──────────────┘
                   │  git push
                   ▼
   ┌──────────────────────────────┐
   │ remanso-cli  (fork: Sequoia) │
   │ local CLI or GitHub Action   │
   │ change-detect · img → blobs  │
   │ writes atUri back            │
   └───────────────┬──────────────┘
                   │  com.atproto.repo.createRecord
                   ▼
   ┌──────────────────────────────────────────────────┐
   │ PROTOCOL — your PDS   (records you own)          │
   │ identity: did:plc:… + handle  (plc.directory)    │
   │ addressed by DID + rkey:                         │
   │   site.standard.document   shared → reach        │
   │   space.remanso.note       custom → rich         │
   └────────────┬─────────────────────────────────┬───┘
                │ firehose / Jetstream            │ listRecords (read)
                ▼                                 ▼
   ┌─────────────────────────┐   ┌────────────────────────────────┐
   │ remanso-jetstream       │   │ APP — many lenses, one source  │
   │ AppView (self-hosted)   │   │  Remanso (remanso.space)       │
   │ Jetstream→SQLite→REST   │──▶│    + Bluesky graph (getFollows)│
   └─────────────────────────┘   │  apoena.dev (static site)      │
                                 │  Leaflet / any standard.site   │
     reuse the Bluesky graph ───▶│  Bluesky & other atproto apps  │
     app.bsky.graph.getFollows   └────────────────────────────────┘

   Self-hosted on Coolify (platform.apoena.dev) + Gitea (git.apoena.dev).
   GitHub = push mirror.
```

## Proposal

| Document | What's in it |
| --- | --- |
| [Abstract & titles](docs/abstract.md) | Title options and the long (detailed) abstract |
| [Outline & format](docs/outline.md) | Timed talk outline, lightning variant, A/V & logistics |
| [Themes & influences](docs/influences.md) | The ideas and people credited on stage |
| [Audience & takeaways](docs/audience.md) | Why now, who it's for, what they leave with |
| [Submission kit](docs/submission.md) | Speaker bio, supporting material, tailoring checklist |

---

*Built on `File > Protocol > App` — own your files, share them over a protocol, read them through any app. Self‑hosted on Coolify + Gitea, GitHub as a push mirror.*

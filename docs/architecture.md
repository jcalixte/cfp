# Architecture at a glance — `File > Protocol > App`

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

> The whole stack is self-hosted: **Coolify** (`platform.apoena.dev`) runs the AppView and apps, **Gitea** (`git.apoena.dev`) hosts the code, with **GitHub** as a push mirror.

# Abstract & title options

*The short abstract is in the [README](../README.md); this file holds the title options and the long (detailed) abstract.*

## Title options

Pick one to fit the venue's tone:

1. **`File > Protocol > App`: How a Note‑Taking Habit Became a Voice I Own**
2. **From Private Garden to Public Voice: Building a Note Habit on the AT Protocol**
3. **Apps Killed the Links: Publishing Your Notes on a Network You Own**
4. **Learn, Think, Write, Share — One `*.pub.md` at a Time**

## Long description *(≈290 words — for the "detailed abstract" field)*

I didn't start writing to have a blog. I started because I was tired of being the quiet one — the person who *felt* something was wrong with an argument but couldn't say why. So since 2021 I've read and written permanent notes, and little by little my voice counted. Five years and 800+ notes later, I had conviction but no place to put it. A private GitHub repo of Markdown is a beautiful garden — and a closed door.

Two ideas opened it. Steph Ango's **"File over app"**: your work should live in durable, open files that outlast any tool. And Dan Abramov's **"A social filesystem"**: the AT Protocol — the open network under Bluesky — gives every person a personal repository of records they own, with apps as mere views over a shared, public filesystem. Put them together and you get the spine of this talk: **`File > Protocol > App`**. Files first. Protocol second. Apps last.

I'll show the working system I built on that idea — **Remanso** — through four concrete beats:

- **Publish as one gesture.** Suffix a note `*.pub.md`, commit, and a small CLI writes it to *your* server. No form, no dashboard.
- **A shared lexicon for reach, a custom one for richness.** I publish to the *shared* `site.standard.document` schema so any reader renders my notes — and keep a richer custom one (`space.remanso.note`) for my own client.
- **Borrow the graph, don't rebuild it.** A reading feed assembled from the Bluesky social graph — I inherited an audience instead of begging for one.
- **Your own AppView.** A tiny firehose consumer, self‑hosted on my own infrastructure.

You'll leave understanding what atproto actually *is*, and with a realistic path to putting your own writing on a network you own. *Learn, Think, Write, Share.*

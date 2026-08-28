# BABYMONSTER Wire

An independent, unofficial English-language fan hub for BABYMONSTER/MONSTIEZ — news translation, release reviews, official-only video curation, a live tour countdown, and a fan quiz, built to run on Google AdSense.

**Not affiliated with, endorsed by, or sponsored by YG Entertainment or the members of BABYMONSTER.**

## What's in this repo

This is a single static page — `index.html` — with everything (HTML, CSS, JS) inlined. No build step, no dependencies, no backend. It's meant to be served as-is by GitHub Pages. This repo follows the same template as [Bangtan Wire](https://fhzl0117-hue.github.io/bangtan-wire/), [Blackpink Wire](https://fhzl0117-hue.github.io/blackpink-wire/), [Stray Kids Wire](https://fhzl0117-hue.github.io/stray-kids-wire/), [aespa Wire](https://fhzl0117-hue.github.io/aespa-wire/), [ENHYPEN Wire](https://fhzl0117-hue.github.io/enhypen-wire/), [SEVENTEEN Wire](https://fhzl0117-hue.github.io/seventeen-wire/), [TWICE Wire](https://fhzl0117-hue.github.io/twice-wire/), [LE SSERAFIM Wire](https://fhzl0117-hue.github.io/lesserafim-wire/), [TXT Wire](https://fhzl0117-hue.github.io/txt-wire/), [(G)I-DLE Wire](https://fhzl0117-hue.github.io/gidle-wire/), [RIIZE Wire](https://fhzl0117-hue.github.io/riize-wire/), [ZEROBASEONE Wire](https://fhzl0117-hue.github.io/zerobaseone-wire/), and [IVE Wire](https://fhzl0117-hue.github.io/ive-wire/) — part of the "Wire" series, one dedicated site per artist.

The page is organized into six "desks," each mapped to a content pillar:

| Desk | Section id | What it does |
|---|---|---|
| 01 · News | `#news` | Translated & summarized news dispatches, each linking to its original source |
| 02 · Review | `#reviews` | Album / track reviews, text only |
| 03 · Screening Room | `#screening` | Official YouTube embeds only — never re-uploaded video |
| 04 · Signal | `#signal` | A live timer that counts down to confirmed future dates, or counts up ("time since") for past ones — auto-converted to the visitor's local timezone |
| 05 · Quiz | `#quiz` | A lightweight interactive quiz, no backend, no data collection |
| 06 · Market | `#market` | Links to official stores (affiliate links go here) |

## A note on accuracy: the seven-member lineup and Rami's hiatus

BABYMONSTER debuted as a seven-member group under YG Entertainment on April 1, 2024, with the *Babymons7er* EP: Ahyeon, Ruka, Pharita, Asa, Rami, Rora, and Chiquita. On May 9, 2025, YG announced that Rami would go on an indefinite hiatus to focus on her health, and she did not join the Asia or North America legs of the *Hello Monsters World Tour* that followed. As of this build (August 2026), she has not returned for any *Choom*-era activity — the EP, the digital single, the Summer Sonic set, or the *Choom World Tour* — and YG has not issued any statement changing her membership status one way or the other. This site treats her as a member on an ongoing, undated hiatus, consistent with the last official word from the company, and will not describe her as having left the group, or as having returned, without a dedicated, corroborated source confirming either. It's a genuinely open situation, not a data error to "fix" — please don't add speculative language about her status (fan theories about departure or a solo transition are widely circulated online but are not confirmed facts).

A side note in the same vein: member RAMI was the one who announced the group's official fandom name, MONSTIEZ, back on July 26, 2024 — "MONS" from BABYMONSTER plus "TIES" for close bonds between the group and fans. That context is worth keeping in mind rather than editing out.

## A note on accuracy: the Choom era and World Tour

Third EP *Choom* (title track "Choom," plus "Moon," "I Like It," and "Locked In") released May 4, 2026, and its title track became the fastest K-pop music video released that year to reach 100 million YouTube views. A digital single, "Sugar Honey Ice Tea," followed on June 8. The *Choom World Tour* — the group's second — opened with three nights at Seoul's Jamsil Indoor Stadium (June 26–28) before a six-city Japanese arena run (Kobe, Fukuoka, Yokohama, Chiba, Nagoya) that sold out across the board, building to the tour's first-ever solo dome shows at Kyocera Dome Osaka on September 22–23. As of this build, the Osaka dome dates are still upcoming, so the Signal desk's Kyocera Dome row is a genuine "time left" countdown rather than "time since." Update it to "time since" once that date passes, and don't add further tour stops (Southeast Asia, Europe, North America, or South America) without a source — none had been announced as of this build.

## manifest.json — K-Wire Network auto-discovery

This repo carries a `manifest.json` at its root so it's automatically picked up by [K-Wire Network](https://fhzl0117-hue.github.io/), the directory hub for the whole "Wire" series. No manual edit to the hub repo is needed — its page fetches this file on every visit and lists this site automatically.

## Updating content

Everything is plain HTML — open `index.html` in any editor and look for the section with the matching `id` (e.g. `<section ... id="news">`) to update copy. There's no CMS yet; each dispatch, review, or signal-desk date is a hand-edited block. See the comments inside the `<script>` tag at the bottom for how the quiz and countdown/elapsed timers work if you need to change their logic — the Signal desk timer auto-detects whether a `data-target` date is in the future (shows "time left") or the past (shows "time since"), so it works either way without further edits.

**Before adding new dates or news items,** verify the underlying facts against a real source and keep the "Read the original source" link pointing at it — that link is what keeps this page compliant with content policies (Google AdSense does not allow re-publishing copyrighted material, and this page's whole design is built around linking out and summarizing instead of reposting).

**Before adding any new YouTube embed,** verify it against the official channel using the oEmbed check: fetch `https://www.youtube.com/oembed?url=https://www.youtube.com/watch?v=<ID>&format=json` and confirm `author_name` is "BABYMONSTER" on channel `@BABYMONSTER` — unlike some other groups in this series, BABYMONSTER uploads through its own dedicated channel rather than a shared label channel, but a plausible-looking title is still not proof by itself. During this build, two other candidate video IDs surfaced in search results under official-looking titles ("BABYMONSTER - CHOOM (OFFICIAL VIDEO M/V)" and a second "CHOOM" M/V listing) but both returned a 404 from the oEmbed endpoint — meaning the videos were unavailable or invalid — and were rejected in favor of the two IDs that returned a clean `author_name: "BABYMONSTER"` response. Both embeds actually used in this build ("Choom" and "Sugar Honey Ice Tea") were verified this way.

## License / ownership

Internal company project. Not licensed for redistribution outside the team without checking with whoever owns this repo.

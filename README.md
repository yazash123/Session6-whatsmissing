# Session 6: what's missing

The House of the People "What's missing?" page, running on its own instead of inside claude.ai.

- **Live page:** https://yazash123.github.io/Session6-whatsmissing/ (room links: add `#g1` to `#g26`; `#supp` opens the supplementary risks, `#example` an example room with five imaginary people)
- **In Webflow:** paste `webflow-embed.html` into one Code Embed in a full-width section (not a Container). Room links work on the Webflow address too, for example `…/your-page#g6`.

## Rooms

Each member picks their room and adds their name. The room sets the cluster, as on the Iceberg tables:

| rooms | cluster |
|---|---|
| 1–4 | Everyone with data |
| 5–8 | Voters and the public |
| 9–12 | Children and learners |
| 13–14 | People at work |
| 15–20 | Civilians in conflict |
| 21–26 | The bodies meant to check |

A member's name and ID are kept under the browser key `hotp-me`, shared with the other HotP activity pages on this site.

## Files

| file | what it is |
|---|---|
| `index.html` | the page. Copied straight from the claude.ai artifact "HotP What's Missing", so don't hand-edit it; make changes in the artifact and copy it over again. |
| `webflow-embed.html` | the one Webflow embed. |

## How it differs from the artifact

Nothing is rewritten. The page has no database yet: everyone's contributions, and the "Our room" tab that brings them together, are kept in each person's own browser (`localStorage`). Sharing a room between members through Firebase is the next step, so for now "Our room" only shows what was added on that computer (or the example room). Outside claude.ai there is no `window.claude`, so the page skips its own **Edit text** bar and is read-only.

## Updating the page

1. Change the artifact in claude.ai.
2. Save its `index.html` over this one and push.
3. GitHub Pages republishes in a minute or two. The Webflow embed points at the live page, so it needs no change. People may need to reload to see it.

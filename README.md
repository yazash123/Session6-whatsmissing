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
| `firebase-config.js` | the Firebase web config (public). |
| `webflow-embed.html` | the one Webflow embed. |

## Live sharing (22 Oct)

Everything members add is shared live with their room through Firestore (project `session-5-activity`, collection `miss-s7`, set by `MISSBOARD` in `index.html`; use `miss-s6` if it runs on a Saturday). There is one document per thing added: a wording (`w<room>-<risk>-<pid>`, one per person and risk), a gap note or a new risk (random ids), or a "kept creeping in" tap (`c<room>-<risk>-<pid>`). Hearts are `st.<pid>`, one per write. Nothing is deleted; removing sets `gone`. The page listens to one room at a time. Others' answers stay hidden until "See what others in your room put" is switched on. The rules are the `missItem` part of `firestore.rules` in the session6-iceberg repo.

`firebase-config.js` is public by design; the rules protect the data. Outside claude.ai there is no `window.claude`, so the page skips its own **Edit text** bar and is read-only.

## Updating the page

1. Change the artifact in claude.ai.
2. Save its `index.html` over this one, put the three Firebase script tags back just above `<script id="app">`, and push.
3. GitHub Pages republishes in a minute or two. The Webflow embed points at the live page, so it needs no change. People may need to reload to see it.

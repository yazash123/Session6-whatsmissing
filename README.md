# Session 6: what's missing

The House of the People "What's missing?" page, running on its own instead of inside claude.ai.

- **Live page:** https://yazash123.github.io/Session6-whatsmissing/ (cluster links: add `#data`, `#voters`, `#kids`, `#work`, `#war` or `#check`; `#supp` opens the supplementary risks)
- **In Webflow:** paste `webflow-embed.html` into one Code Embed in a full-width section (not a Container). Cluster links work on the Webflow address too, for example `…/your-page#kids`.

## Files

| file | what it is |
|---|---|
| `index.html` | the page. Copied straight from the claude.ai artifact "HotP What's Missing", so don't hand-edit it; make changes in the artifact and copy it over again. |
| `webflow-embed.html` | the one Webflow embed. |

## How it differs from the artifact

Nothing is rewritten. The page has no database: each person's answers are kept in their own browser (`localStorage`), and "the record" at the end is how they get them out. Outside claude.ai there is no `window.claude`, so the page skips its own **Edit text** bar and is read-only.

That also means there is no Firebase and no rules file here, unlike Session 5.

## Updating the page

1. Change the artifact in claude.ai.
2. Save its `index.html` over this one and push.
3. GitHub Pages republishes in a minute or two. The Webflow embed points at the live page, so it needs no change. People may need to reload to see it.

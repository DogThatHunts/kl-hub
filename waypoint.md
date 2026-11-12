# Waypoint: kl-hub

## What was done (2026-11-12 session)

- Created this new, dedicated public repo and GitHub Pages site as a
  higher-level index above the individual per-speaker research projects,
  per user request: "a higher level index, with tiles for: KL on RiceRadio,
  KL on Crrow777, Roger Sayles, Brandon Joe, Dave Champion, the common
  citation register."
- Before building, planned and asked clarifying questions (see decisions
  below) rather than assuming, since 3 of the 6 requested tiles had no
  existing public destination to link to.
- Styled per the user's request to match
  `https://dogthathunts.github.io/transcript-summaries/posts/kl-great-birth-certificate-deception-w-dr-kl-beneficiary-lesson-2-2022-1264.html`
  — fetched that site's shared `assets/style.css`, confirmed it already has
  a `.post-card`/`.posts-grid` tile-index pattern (built for that site's own
  index page) in addition to the article/hero styling, and vendored a copy
  into this repo (`assets/style.css`) rather than linking the live file, so
  this page keeps rendering even if the source stylesheet changes later.
  Added a small block of hub-specific CSS at the end of that vendored copy
  (not upstream) for tile states the source site doesn't have:
  `.is-placeholder`, `.post-card-tag.is-pending`, `.post-card-tag.is-private`.

### Decisions made via AskUserQuestion (all picked the recommended option)

1. **Hosting**: new dedicated repo (`DogThatHunts/kl-hub`), not the special
   `dogthathunts.github.io` user-page repo (which doesn't exist and would
   have permanently claimed the bare root domain for this purpose).
2. **Roger Sayles / Brandon Joe** (neither has a published project):
   placeholder tiles, shown but not linked, rather than building them out
   now or omitting them.
3. **Common Citation Register** (repo exists but is private, no Pages
   site): non-linked descriptive tile, rather than linking to the private
   repo (which would 404 for everyone but the owner) or building a new
   public read-only register page.
4. **CSS**: vendor a copy into this repo rather than linking the live
   `transcript-summaries` stylesheet directly.

### What was researched to inform those decisions

- `KL_on_RiceRadio`, `KL_on_Crrow`, `dave_champion`: all three already live
  on GitHub Pages (confirmed via `gh api repos/.../pages`).
- `citation-register`: repo exists, confirmed **private**, no Pages site
  (404 on the pages API).
- **Roger Sayles**: no project anywhere in `~/Projects/`. Only trace found
  is a single transcript-classification mention in
  `~/Projects/transcription-agent/booklinks/measurement/classified_2026-09-20.jsonl`
  — "author and researcher Roger Sayles" / his book *From Sovereign to
  Serf*. Nothing has been built on him yet.
- **Brandon Joe** = **Brandon Joe Williams**, presenter of "Contract Killer
  Course 3.0" (CKC 3.0). A real, substantial analysis already exists —
  `~/Projects/transcription-agent/CKC3_FRAMEWORK.md` (six-layer pseudolegal
  framework built on an explicit racial-citizenship-class premise) and
  `CKC3_CITATIONS.md` — but `transcription-agent` is a **private** repo and
  neither file has been published anywhere public. If/when this project
  gets its own public site (mirroring the `KL_on_*`/`dave_champion`
  pattern), that existing framework doc is the starting point, not a
  from-scratch pass.

## Layout

```
index.html       # the hub page — hero + 6-tile posts-grid + footer
assets/
  style.css      # vendored copy of transcript-summaries' shared stylesheet
                  # (do not hand-edit the vendored portion; re-sync instead,
                  # see README.md for the resync command) + a small
                  # kl-hub-only addition at the bottom for placeholder/
                  # private tile states
README.md        # tile status table + resync instructions
waypoint.md       # this file
```

## Still open

- **Roger Sayles tile**: still a placeholder. No transcripts, no ideas
  summary, no citation sidecar, no site exist yet. Whenever that project is
  started, it would follow the same shape as `KL_on_RiceRadio`
  (`transcripts/TXT/` + `prompts/` + `summaries/` + `summaries_html/` +
  `index.html`/`style.css`), and this hub's tile just needs its
  `is-placeholder` div swapped for a real `<a>` link once a Pages site
  exists.
- **Brandon Joe tile**: still a placeholder, but unlike Roger Sayles there's
  real underlying analysis to draw on (`transcription-agent/CKC3_FRAMEWORK.md`,
  `CKC3_CITATIONS.md`) — the work here would be *publishing* that existing
  analysis as its own project (new repo + Pages site, or folding into an
  existing one), not starting the analysis from scratch. Content note for
  whoever does this: the course is explicitly, unapologetically racial in
  its doctrine (a claimed white-only citizenship class) — flagged in the
  source framework doc as foundational, not incidental, so any public
  write-up needs to represent that plainly rather than soften it.
- **Common Citation Register tile**: still non-linked. No decision has been
  made about whether this register should ever get a public read-only page
  — if that changes, revisit option 3 from this session ("build a public
  read-only register page, similar to the citations-sidecar tables already
  built for the KL projects").
- **No waypoint cross-link added** in the three existing per-project repos
  (`KL_on_RiceRadio`, `KL_on_Crrow`, `dave_champion`) pointing back up to
  this new hub — each project's own `README.md`/waypoint still stands alone.
  Minor, but worth a one-line mention in each if this hub becomes the
  primary entry point people land on first.

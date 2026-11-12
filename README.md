# kl-hub

A single landing page indexing the KL / sovereign-citizen / pseudolegal
research projects, all of which share one citation-verification process
against a common (private) citation register.

Published via GitHub Pages at <https://dogthathunts.github.io/kl-hub/>.

## Tiles

| Project | Status | Link |
|---|---|---|
| KL on RiceRadio | Live | <https://dogthathunts.github.io/KL_on_RiceRadio/> |
| KL on Crrow777 | Live | <https://dogthathunts.github.io/KL_on_Crrow/> |
| Dave Champion | Live | <https://dogthathunts.github.io/dave_champion/> |
| Roger Sayles | Coming soon | no project yet |
| Brandon Joe (Williams) | Coming soon | no published site yet (internal notes only, in the private `transcription-agent` repo) |
| Common Citation Register | Private | no public page |

## Layout

```
index.html       # the hub page itself
assets/
  style.css      # vendored copy of transcript-summaries' shared stylesheet,
                  # plus a small addition at the bottom for placeholder/
                  # private tile states (.is-placeholder, .is-pending, .is-private)
```

`style.css` is a vendored copy, not a live link, so this page keeps working
even if the source stylesheet changes. Re-sync manually if the upstream
palette/design changes:

```
curl -s https://dogthathunts.github.io/transcript-summaries/assets/style.css -o assets/style.css
# then re-apply the kl-hub-specific additions at the bottom of the file
```

# Make arXiv Red Again

A tiny Chrome extension that restores arXiv's iconic **red** site header,
reverting the 2026 redesign that repainted the banner black.

It's pure CSS — no JavaScript, no permissions, no network access. It only
touches the header (`.ds-site-header`) on `arxiv.org`.

## Install (load unpacked)

1. Open `chrome://extensions`.
2. Toggle **Developer mode** on (top-right).
3. Click **Load unpacked** and select this `arxiv-red-banner/` folder.
4. Visit any page on <https://arxiv.org> — the banner is red again.

To update after editing `arxiv-red.css`, hit the **↻ reload** icon on the
extension card and refresh the arXiv tab.

## What it changes

| Element | Before (redesign) | After |
| --- | --- | --- |
| Header background | `#1c1a17` (`--arxiv-ink`, black) | `#b31b1b` (arXiv red) |
| Logo wordmark | red + warm-grey (for dark bar) | solid white |
| Nav links | dim grey | white |
| Link hover | brown-black | darker red (`#8f1414`) |

## Customizing the red

Prefer a different shade? Edit the two `#b31b1b` values in `arxiv-red.css`
(the banner and the mobile menu), reload the extension, and refresh.

## Files

- `manifest.json` — Manifest V3 declaration; injects the CSS on `*.arxiv.org`.
- `arxiv-red.css` — the style overrides.

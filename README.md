# Make arXiv Red Again

A tiny Chrome extension that restores arXiv's iconic **red** site header,
reverting the 2026 redesign that repainted the banner black.

It's pure CSS — no JavaScript, no permissions, no network access. It only
touches the header (`.ds-site-header`) on `arxiv.org`.

Works in both Chrome and Firefox from the same folder — it's Manifest V3
with no background script or permissions, so nothing browser-specific is
needed beyond the Firefox add-on `id` (which Chrome simply ignores).

### Chrome / Edge / Brave

1. Open `chrome://extensions`.
2. Toggle **Developer mode** on (top-right).
3. Click **Load unpacked** and select this repo folder.
4. Visit any page on <https://arxiv.org> — the banner is red again.

To update after editing `arxiv-red.css`, hit the **↻ reload** icon on the
extension card and refresh the arXiv tab.

### Firefox

1. Open `about:debugging#/runtime/this-firefox`.
2. Click **Load Temporary Add-on…**.
3. Select the `manifest.json` file in this repo folder.
4. Visit any page on <https://arxiv.org>.

Temporary add-ons are removed when Firefox restarts. To install permanently
you must sign the package via [AMO](https://addons.mozilla.org) — the
`browser_specific_settings.gecko.id` in `manifest.json` is already set up for
that.

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

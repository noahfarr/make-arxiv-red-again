# Make arXiv Red Again

A tiny Chrome/Firefox extension that restores arXiv's iconic **red** header,
reverting the 2026 redesign that turned the banner black.

Pure CSS. No JavaScript, no permissions, no network access.

## Install

**Chrome / Edge / Brave**: go to `chrome://extensions`, turn on
**Developer mode**, click **Load unpacked**, and pick this folder.

**Firefox**: go to `about:debugging#/runtime/this-firefox`, click
**Load Temporary Add-on**, and pick `manifest.json`.

Then open any page on <https://arxiv.org>.

## Customize

Prefer a different shade? Change the `#b31b1b` values in `arxiv-red.css`
and reload the extension.

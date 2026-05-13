# FFmpeg Intro

![FFmpeg Intro — A practical introduction to FFmpeg](og-image.png)

A practical introduction to [FFmpeg](https://ffmpeg.org/) — what it is, where it came from, and how to use it for the most common audio and video tasks. Built around real command examples you can adapt as you go.

## Access FFmpeg Intro

- **Live:** https://timmolab.github.io/ffmpeg-intro/
- **Locally:** clone the repo and open `index.html` in any modern browser. Each page is self-contained — no build step, no server needed.

## Pages

The site has two pages, both sharing the same brand mark, theme system, and right-side rail.

- **`index.html`** — the main guide. Sixteen chapters from "What is FFmpeg?" through Glossary and Useful links.
- **`one-liners.html`** — a standalone cheat sheet of ten drop-in commands for the most common tasks. Each row has an **Explain** toggle that drops down a flag-by-flag breakdown.

Both pages cross-link to each other through the right-rail **Pages** panel (visible at viewports ≥ 1440px).

## What's in the guide (`index.html`)

1. What is FFmpeg?
2. A bit of history
3. Installing it (Windows via gyan.dev; pointers for Linux / macOS)
4. Key concepts — command structure, streams inside a container, container vs. codec
5. Flag cheat-sheet
6. First commands — convert, resize, extract / remove audio
7. Capturing from a device (Windows DirectShow)
8. Cut, crop, snapshot
9. Working with frames
10. CPU vs GPU encoding
11. Metadata and FFprobe basics
12. VMAF — measuring perceptual video quality
13. Common error messages
14. Performance tuning & presets
15. Glossary
16. Useful links — official FFmpeg refs, VMAF resources, hardware-encoding pointers, related tools (VLC, OBS, Shotcut, Audacity)

Each command example has an *Explain this command* expandable panel that breaks down every flag.

## What's on the cheat sheet (`one-liners.html`)

A compact, scannable table of ffmpeg recipes for the things most people Google over and over:

- Convert to MP4 (H.264 + AAC)
- Trim a clip (fast, keyframe-aligned)
- Remove the audio track
- Extract audio to MP3
- Resize to 720p (keep aspect)
- Make a GIF
- Normalize loudness (EBU R128)
- Single frame at a timestamp
- Contact-sheet thumbnails
- Inspect a file with `ffprobe`

Each row exposes a copy-to-clipboard button and an **Explain** toggle that drops down a `<dl>`-style flag-by-flag breakdown.

## Layout & features

- **Left sidebar (sticky)** — brand mark + chapter table of contents. The active chapter highlights as you scroll on `index.html`. Below 900px the sidebar collapses into a tap-to-expand panel.
- **Right rail (≥ 1440px)** — theme toggle, **Pages** panel (current page marked active), **Reference Links** (FFmpeg docs / filters reference / wiki), and a meta block with the GitHub link and last-updated date.
- **Theme** — light / dark toggle. First visit honours `prefers-color-scheme`; subsequent visits remember your choice via `localStorage`.
- **Code blocks** — click-to-copy icon button on every `<pre>`, with a tooltip that swaps to "Command copied to clipboard" on success.
- **Headings** — every chapter heading has a copyable deep-link anchor.
- **Brand** — a fast-forward (`▶▶`) glyph in the page favicon, sidebar mark, and hero `<h1>` (clickable; acts as a permalink to the top of the page).
- **Mobile** — collapsible TOC, tighter padding, table cells that wrap instead of clipping. Right rail is hidden; the fixed top-right theme toggle reappears so you still have access.

## Repo layout

```
index.html       Main guide (single file, all CSS + JS inline)
one-liners.html  Cheat-sheet page (same structure)
og-image.png     1200×630 social preview card
LICENSE          MIT
README.md        This file
```

## Updating the date

The `Updated YYYY-MM-DD` label that appears in the right rail and footer is driven by a single `UPDATED` constant near the top of each page's inline `<script>` block. Bump it in both files when you ship a change you want to advertise.

## Suggestions or fixes

Open an issue or pull request — corrections, clarifications, and additional examples are welcome.

## License

Released under the [MIT License](LICENSE).

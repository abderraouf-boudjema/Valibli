# Package contents & provenance notes

This archive contains everything from this drafting session, organized as a
small project folder. A few things worth knowing before you use it:

## What's included

- `README.md` — the full project write-up (see there for the design
  rationale, the relationship to the original TUSF proposal, and what this
  draft resolves).
- `converter.html` — the interactive Latin-to-Valbli converter. Self-contained,
  no build step; just open it in a browser.
- `images/alphabet-specimen.svg` — a chart of all 25 letters, generated
  **programmatically from the actual glyph path data embedded in
  `converter.html`** (the same `CONSONANT_PATHS` / vowel paths the converter
  itself uses to draw). This is not a redrawn or approximated chart — it's
  the real letterforms, laid out as a reference sheet.
- `images/example-sutra.svg`, `images/example-tavla.svg`,
  `images/example-mi-tavla-do.svg` — the worked examples from the README
  (§4 and §7), rendered by running the same recursive block-layout algorithm
  used inside `converter.html` against those specific words, so the images
  match what the converter would actually produce for that input.
- `LICENSE` — see below; the licensing situation here is genuinely unresolved,
  not just left out by omission.

## What's *not* included, and why

- **`Sefta.sfdir` (the FontForge font source)** is not included. It's
  referenced throughout the README and in `converter.html`'s own comments as
  the source of the real consonant letterforms, but the actual font-source
  file was never provided in this conversation/session — only the already-
  extracted SVG path data baked into `converter.html`. If you have access to
  the original TUSF repository, that's the place to get the real
  `Sefta.sfdir`.
- No raster (PNG/JPG) alphabet chart from the *original* proposal is
  included either, for the same reason: it wasn't available to reproduce
  from, and recreating it from memory would risk misrepresenting the
  original author's actual artwork. What you get instead are the freshly
  generated SVGs described above, built directly from real path data.

## License status

This project is a derivative of TUSF's original, informally-licensed gist
proposal. No explicit license was stated for that original work at the time
of writing. Rather than assert a license this project isn't in a position to
grant, `LICENSE` documents that situation honestly instead of picking an
arbitrary one. If you plan to redistribute or build on this, please read it.

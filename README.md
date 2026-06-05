# quintilianinc.com

Static marketing + portfolio site for **Quintilian, Inc.** Hand-coded HTML/CSS,
no build step. Hosted on Netlify; deploys automatically on every push to `main`.

## Structure

```
/                  index.html        — homepage (dark theme, AI-consulting)
/work              work/             — public portfolio (Illustration, Brand,
                                       Email, Product, Sanctified Souls, Catholic Apps)
/client-work       client-work/      — PASSWORD-PROTECTED. Pitch decks only.
/speedread         speedread/        — Speed Read Anything app landing page
images/  app-mockups/  placeholders/ — assets (referenced by relative paths)
```

Each page is a single self-contained `index.html` with inline `<style>`.
The homepage uses a warm-dark palette; the Work / Client Work pages use a
cream palette (`--cream #ECDFCF`, `--ink #1A1A1A`, fonts PT Serif + Inter).

## Editing

Edit the HTML files directly. Image paths are **relative** to each page, e.g.
`work/index.html` references `images/projects/...` and `app-mockups/...`.

## Client Work password

`/client-work` is gated by a client-side JavaScript password screen.
Password: `quintilian-portfolio-2026` (set in the `<script>` at the bottom of
`client-work/index.html`). Note: this is a soft gate — fine for a
"shared by request" portfolio, but not server-side security.

## Deploying

Netlify is connected to this repo. **Push to `main` → Netlify rebuilds and
publishes automatically.** No build command (static files); publish directory
is the repo root.

Manual fallback (if needed): drag this folder onto the Netlify **Deploys** page,
or run `netlify deploy --prod --dir .`.

## TODO / notes

- Some portfolio images (e.g. `work/images/projects/book-covers-publishing/`)
  are 19–24 MB — compress for faster page loads.
- `work/images/new-work/new-022.png` is missing (404 on source) — one empty grid slot.
- Pitch-deck PDFs are placeholders; drop real PDFs into `client-work/` and wire
  the `<object>`/embed when ready.

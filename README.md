# Paté for my Caté

One-page brand site for **Paté for my Caté** — hand-spooned, French-style cat paté at affordable prices. Vibe: Viennetta-1990s luxury (deep navy + antique gold + Playfair script).

## Structure

```
.
├── index.html        v.I — original one-pager (tin packaging, romantic founder story)
├── images.md         5 t2i prompts for v.I
├── images/           v.I images (image-01 … image-05)
├── v2/
│   ├── index.html    v.II — Snap-Pack Edition (Le Comte mascot, Robin-Leach voice)
│   ├── images.md     5 t2i prompts for v.II (new packaging + mascot)
│   └── images/       v.II images (drop image-01 … image-05 here when generated)
├── netlify.toml      Netlify publish config (publish = ".")
└── README.md
```

Both versions deploy from the same Netlify site. v.I is at `/`, v.II is at `/v2/`. They cross-link in their footers.

## Local preview

```bash
open index.html
```

Or with a tiny local server:

```bash
python3 -m http.server 8000
# then http://localhost:8000
```

## Deploy to Netlify

This is a static site — no build step.

**Option A — git-connected (recommended):**
1. Push this repo to GitHub.
2. In Netlify: *Add new site → Import from GitHub → pick this repo*.
3. Build command: *(leave blank)*. Publish directory: `.` (already set in `netlify.toml`).
4. Deploy.

**Option B — drag & drop:**
1. Zip the folder.
2. Drop it onto https://app.netlify.com/drop.

## Adding the images

Generate the 5 images in `images.md` (Image Generator at `/admin/image-generator` on the Lead Billing Platform), drop them into `/images/`, then update the placeholder `<div class="ph">` blocks in `index.html` to real `<img>` tags. The placeholder paths in the HTML already match the filenames suggested above.

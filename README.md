# Paté for my Caté

One-page brand site for **Paté for my Caté** — hand-spooned, French-style cat paté at affordable prices. Vibe: Viennetta-1990s luxury (deep navy + antique gold + Playfair script).

## Structure

```
.
├── index.html        Single-page site (inline CSS, no build step)
├── images.md         5 nano-banana-2 text-to-image prompts for hero/product/lifestyle imagery
├── netlify.toml      Netlify publish config
└── images/           Place generated images here
    ├── 01-hero-le-chat-royal.jpg
    ├── 02a-saumon.jpg
    ├── 02b-thon.jpg
    ├── 02c-poulet.jpg
    └── 05-latelier-kitchen.jpg
```

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

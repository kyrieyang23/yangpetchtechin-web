# yangpetchtechin.com

Personal landing page for Yang Petchtechin.

---

## Quick edits

### 1. Change content (name, bio, links)

Open `index.html` and find the `CONFIG` object near the bottom, inside `<script>`:

```js
const CONFIG = {
  profile: {
    name: "Yang Petchtechin",
    headline: "Don't follow your dream\nfollow me on Instagram",
    bio: "Bangkok based. Investor...",
  },
  links: {
    tiktok: "https://tiktok.com/@your-handle",   // ← update this
    instagram: "https://instagram.com/your-handle", // ← and this
    ...
  },
  ...
}
```

Save and refresh. No build step needed.

### 2. Change colors / style

Find `:root { ... }` near the top of the `<style>` tag:

```css
:root {
  --accent-orange: #F0915A;   /* main CTA color */
  --accent-gold: #E8C065;     /* cards, accents */
  --accent-rose: #D4756A;     /* meet card */
  --bg-primary: #0C0A08;      /* page background */
  ...
}
```

Every color in the page flows from these variables — change one line, it updates everywhere.

### 3. Add your photo

1. Export a portrait photo (3:4 ratio recommended, min 800px wide)
2. Save it as `images/profile.jpg`
3. Refresh the page — the placeholder disappears automatically

### 4. Adjust particles

In `CONFIG.particles`:
- `count`: number of floating dots (default 90, mobile auto-reduces to 40)
- `speed`: how fast they drift (default 0.25)
- `connectionDistance`: how close particles need to be to draw a line (default 120)
- `colors`: array of hex colors for particles

---

## Deploy to Cloudflare Pages

1. Push this folder to a GitHub repo
2. Go to [Cloudflare Pages](https://pages.cloudflare.com/)
3. Click **Create a project** → **Connect to Git**
4. Select your repo
5. Build settings:
   - **Framework preset:** None
   - **Build command:** *(leave empty)*
   - **Build output directory:** `/` (root)
6. Click **Save and Deploy**
7. Add your custom domain `yangpetchtechin.com` in the Pages project settings

That's it — Cloudflare serves the static file globally with HTTPS.

---

## File structure

```
yangpetchtechin-web/
├── index.html          ← everything is here (CSS + JS inline)
├── images/
│   ├── README.md       ← photo instructions
│   └── profile.jpg     ← add your photo here
└── README.md           ← this file
```

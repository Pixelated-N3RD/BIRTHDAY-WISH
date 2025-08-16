# Birthday Wish — Sudu × Pishan

Interactive birthday card: a cute two-character chat that advances on click.  
Made with plain HTML/CSS/JS — no frameworks, no build.

## Live
After enabling GitHub Pages, your site will be here:

```
https://<your-username>.github.io/<your-repo>/
```

## Features
- Click anywhere to advance the conversation
- Typing effect with click-to-complete for each line
- Left/right bubbles mapped to **Sudu** (left) and **Pishan** (right)
- Soft click sound, floating heart confetti, sweet end card (headline: “Made for **you** by **love**”)
- “made with love for your birthday” footer
- Light theme with CSS polka-dot “sky” and “floor” (no background image file needed)
- Single file (`index.html`) + two character images
- Includes Page 14: **Pishan:** “Happy birthday Sudu.” → **Sudu:** “Thanks Ishan.”

## Files
```
index.html        # the app (single file)
S.webp / S.png    # Sudu (left). Use one or both
I.webp / I.png    # Pishan (right). Use one or both
.nojekyll         # optional for GitHub Pages (empty file)
README.md         # this file
```

## Run locally
Just double-click `index.html` (or open it in any browser).  
Make sure your image filenames match exactly (`S.webp`/`I.webp` or PNGs).

## Customize
Open `index.html` and find:

```js
const PAGES = [ /* …pages… */ ];
```

Each page is two lines:
```js
{ lines: [
  { speaker: 'friend', text: '“How’s life treating you?”' },
  { speaker: 'me',     text: '“Like it’s mad I owe it money.”' }
]}
```

- `speaker: 'friend'` → **Sudu** (left)  
- `speaker: 'me'` → **Pishan** (right)

Names shown under the avatars are set near the top:
```js
const meName = 'Pishan';
const friendName = 'Sudu';
```

### Tweak look & feel
In the `<style>` block:
- Bubble size: `font-size: clamp(18px, 2.6vw, 22px)` and `padding: 22px 26px`
- Bring bubbles closer/further from characters: edit spacing in `.chat` and `.chars`
- Background split height: `--sky-h: min(60vh, 520px)`

### Footer / end card
- Footer text: **made with love for your birthday** (bottom of the file).  
- End-card headline set to *“Made for you by love”*.

## Deploy to GitHub Pages
1. Create a **public** repo and upload the files (keep the name `index.html` lowercase).
2. (Optional) Add an empty file named `.nojekyll` in the repo root.
3. **Settings → Pages**
   - Source: **Deploy from a branch**
   - Branch: `main` • Folder: `/ (root)` → **Save**
4. Wait a minute; GitHub will show your site URL on that page.

## Troubleshooting
- **Blank page / 404**: `index.html` must be lowercase and in the repo root.
- **Images not showing**: filenames are case-sensitive (`S.webp`, `I.webp`).
- **Stale content**: hard refresh (**Ctrl/Cmd+Shift+R**).

## License
MIT — use and adapt freely. 

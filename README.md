# 😹💍 MRSCASHCAT — the First Lady of the Robinhood Chain

A maximum-chaos meme site for **$MRSCASHCAT**. 100% static — no build step, no npm, no framework.
One `index.html` + an `assets/` folder. That's the whole site. MEOW.

---

## 🚨 THE ONE THING YOU NEED TO EDIT AT LAUNCH

Open **`index.html`** and search for **`EDIT ME`** (top of the big `<script>` block — the `CA:` line is ~line 843):

```js
const CONFIG = {
  CA: "0x0000000000000000000000000000000000FAKE",   //  ←←← PASTE REAL CA HERE
  TICKER: "$MRSCASHCAT",
  X_URL: "",          // e.g. "https://x.com/mrscashcat"
  TELEGRAM_URL: "",   // e.g. "https://t.me/mrscashcat"
  DEX_URL: "",        // e.g. your dexscreener / dex link — buy buttons use this once set
};
```

**How it behaves:**
- While `CA` contains the word `FAKE` → the whole site runs in **"soon™" mode**
  ("she's doing her makeup 💅" everywhere, copy button jokes instead of copying).
- Paste the real contract address into that ONE line → the CA appears **everywhere
  automatically** (hero pill, how-to-buy box, ticker) and the copy buttons start copying it.
- Fill `X_URL` / `TELEGRAM_URL` / `DEX_URL` → footer buttons link out and every
  **BUY** button opens the DEX. Leave them empty → funny "not public yet" toasts.

No other edits needed. Ever.

---

## 🚀 Deploy

### Option A — GitHub Pages
1. Create a repo (e.g. `mrscashcat`), push these files (`index.html`, `assets/`, `README.md`).
2. Repo **Settings → Pages → Source: Deploy from a branch → main / (root)** → Save.
3. Site goes live at `https://<user>.github.io/mrscashcat/`. Point your domain via
   **Settings → Pages → Custom domain** if you want.

### Option B — Vercel (free tier)
1. `vercel.com` → **Add New Project** → import the repo (or just drag-and-drop this folder).
2. Framework preset: **Other**. No build command. Output directory: root.
3. Deploy → point your domain in **Settings → Domains**. Done.

Both work identically — it's plain static files.

> **Tip:** after deploying, update the `og:image` meta tag in `<head>` to your absolute URL
> (e.g. `https://mrscashcat.xyz/assets/banner.jpg`) so link previews on X/Telegram show the banner.

---

## 🔊 Sound

Browsers block audio until the user interacts. The **MEOW: ON/OFF** toggle in the nav arms
the sound engine AND starts **the Meow Song** — a looping chiptune (kick, bassline, hi-hats,
and a meow-synth lead singing an original melody) generated live in WebAudio. No audio files,
no copyright, loops forever. Clicks add synth meows/chirps on top; the dramatic First Lady
address ducks the song while she speaks. Default is OFF; a hint bubble nudges visitors after
their first click.

## 🥚 Easter eggs
- Click her face in the hero **5 times** → MAXIMUM MEOW (cat rain + royal address, if sound is on)
- Type **`meow`** anywhere on the page → same
- Click the walking pixel cats → they panic
- Open the browser console 👀

## 🎨 Customizing the chaos
- Ticker phrases → `tickerWords` array in the script
- Her speech-bubble lines → `LINES` array
- Walking-cat frequency → `walkerLoop()` timings

## 🙏 Credits
- Motion effects adapted from [nexu-io/motion-anything](https://github.com/nexu-io/motion-anything)
  recipe library (Apache-2.0): silk, pixel-blast, rotating/decrypted/falling/circular/shiny/glitch
  text, count-up, bounce-cards, star-border, electric-border, elastic-slider, image-trail,
  click-spark, like-burst.
- Fonts: Luckiest Guy, Comic Neue, Press Start 2P (Google Fonts).

*This is a parody meme site. Not affiliated with Robinhood. Not financial advice. The utility is wife.*

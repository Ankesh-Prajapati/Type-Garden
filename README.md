# Type Garden

A single-file, browser-based typing toy: every letter you type grows vines, leaves and flowers around it. Cut a word with space, wither it with backspace, and watch bees, butterflies and dragonflies drop by.

> **Inspired by [Type Garden](https://type-garden.vercel.app/) by [Akshat Agarwal (@art_akshat)](https://x.com/art_akshat).**
> This is an independent, self-contained port with extra features. All credit for the original concept and design goes to the original creator. Please visit and support the original:
>
> - Original website: https://type-garden.vercel.app/
> - Creator on X: https://x.com/art_akshat

## Run it

No build step and no dependencies. Open `type-garden.html` in a modern browser (Chrome, Edge, Firefox, Safari). An internet connection is only needed to load the Google Fonts (Playfair Display and DM Mono); without it, system fallback fonts are used.

## Controls

| Action | Result |
|---|---|
| Type | Letters grow vines, leaves and blooms |
| Space | Cuts the word and sprouts end blooms |
| Backspace | Withers the last letter |
| Enter | Clears the garden |
| Click / tap the canvas | Calls a visitor (butterfly, bee or dragonfly) |
| Move the cursor | Flowers and stems lean toward it |
| Ctrl/Cmd + S | Save PNG (add Shift for SVG) |

On phones, tap to open the keyboard; tap the canvas again to call a visitor.

## Features

- **Six flower types:** rose, peony, tulip, daisy, poppy and bellflower, each word with its own favourite.
- **Ten fonts:** Playfair Display (default), DM Serif Display, Abril Fatface, Bodoni Moda, Fraunces, Cormorant Garamond, Pacifico, Caveat, Archivo Black and Bebas Neue. Pick from the dropdown in the Type bar or the Font list in Poster; spacing and the garden re-fit to each face, and SVG export keeps the chosen font. Fonts load from Google Fonts, so go online once for them to appear.
- **Ten palettes:** Rose noir, Paper, Midnight, Citrus, Orchid, Moss, Tomato, Butter, Blush and Mono.
- **Overlap avoidance:** blooms keep clear of each other. Newer blooms shrink to fit, or are dropped if there is no room.
- **Visitors:** butterflies, bees and dragonflies fly in on their own or on click, land on blooms, hop between them, then leave.
- **Soft sound:** a pentatonic chime per keypress (toggle with the SOUND button).
- **Poster mode:** animated loops with seven motion presets (Breathe, Grow & wither, Typed, Gust, Reach, Scatter, Visitors), in four sizes: Square (1080 × 1080), Phone (1080 × 1920), Desktop (1920 × 1080) and Ultrawide (2560 × 1080).
- **Export:** PNG and SVG from the typing view; MP4/WebM video and PNG frame ZIP from Poster mode.

## Live wallpaper

1. Switch to **Poster**, type your words and pick a motion and palette.
2. Choose a **Size**: Phone (9:16) for mobile wallpapers, Desktop (16:9) or Ultrawide (21:9) for monitors.
3. Click **Export MP4/WebM loop** and drop the video into a live-wallpaper app of your choice.

The format depends on your browser: Chrome and Edge export MP4 where supported; otherwise WebM. Every loop is seamless and 30 fps.

## Customise

Edit the `CONFIG` block at the top of the script in `type-garden.html`:

| Option | What it does |
|---|---|
| `boil`, `boilMs` | Hand-drawn shiver on letters and stems |
| `recoil`, `bounce`, `sway`, `speed` | Spring, overshoot, idle breeze and growth tempo |
| `density` | Amount of leaves, branches and bridges (0.5 – 1.6) |
| `flowers` | How often each flower type is picked (0 removes it) |
| `avoidOverlap` | Keep blooms from piling on top of each other |
| `insects` | Visitor mix, e.g. `{ butterfly: 1, bee: 1.2, dragonfly: 0.5 }` (0 removes one) |
| `ambient`, `ambientEvery` | Whether visitors arrive on their own, and how often (ms) |
| `sound`, `volume` | Chime on/off and loudness |
| `showHint` | Show the key hints and export bar |

## Tech

Plain JavaScript and the Canvas 2D API in one HTML file. The interface uses DM Mono; the type face is your choice from ten fonts (see Features).

## Credits

- **Original concept and design:** [Akshat Agarwal](https://x.com/art_akshat), via [Type Garden](https://type-garden.vercel.app/).
- **This port:** a self-contained re-implementation with overlap avoidance and bee/dragonfly visitors added.

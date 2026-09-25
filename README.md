# 領域展開 — Domain Expansion

An immersive scroll experience recreating **Ryomen Sukuna's Domain Expansion** from *Jujutsu Kaisen*. Built with vanilla HTML/CSS/JS, featuring a custom canvas lightning engine and GSAP scroll animations.

## Demo

Open `index.html` in a modern browser. Best experienced on desktop with a scroll wheel.
Just cheak this link 🔗 [https://losxinfinity.github.io/-Domain-Expansion-Sukuna/](url)

## Features

- **Custom Lightning Engine** — Fractal midpoint-displacement channels, white-hot cores, violet glow, recursive branches, multi-restrike flicker, and ambient storm layers. Zero image assets for lightning.
- **Cinematic Scroll Flow** — Hero video → hands forming sign → full-screen thunder → temple parallax + character reveal
- **Parallax Depth** — Temple background and character move at different speeds for 3D depth
- **Reduced Motion Support** — Respects `prefers-reduced-motion`
- **No Build Step** — Single HTML file + assets, runs anywhere

## Assets

| File | Purpose | Specs |
|------|---------|-------|
| `hero.mp4` | Hero background video (looping) | Dark/moody, 1920×1080 recommended |
| `1.png` | Left hand (reaching right) | Transparent PNG |
| `2.png` | Right hand (reaching left) | Transparent PNG |
| `3.png` | Formed hand sign | Transparent PNG, ~1500×550 |
| `4.png` | Character full body | Transparent/dark PNG, ~900×1600 |
| `5.png` | Temple / domain background | Transparent PNG, ~1500×950 |
| `6.png` | Title art "DOMAIN EXPANSION" | Transparent PNG, ~680×350 |

> **Note:** Placeholder assets are included. Replace with your own for production use.

## Tech Stack

- **GSAP 3.12** + ScrollTrigger (via CDN)
- **Vanilla JS** — Canvas 2D API for lightning
- **CSS Custom Properties** — Theming via `:root`
- **Google Fonts** — Rajdhani + Zen Old Mincho

## Customization

### Colors
Edit CSS custom properties in `:root`:
```css
:root {
  --void: #06030c;      /* Deep background */
  --violet: #8b5cf6;    /* Primary accent */
  --violet-hi: #c4b5fd; /* Highlight */
  --bone: #ded7ec;      /* Text primary */
  --dim: #6e6390;       /* Text muted */
}
```

### Kanji Text
Search for `kanjiRail` and `kanjiCorner` in `index.html` to edit the vertical rails and corner labels.

### Lightning Intensity
Adjust `stormLevel` timeline calls (e.g., `setStorm(3.5, 1)`) and `skyBolt`/`tearBolt` parameters.

## Browser Support

- Chrome 90+
- Firefox 88+
- Safari 15+
- Edge 90+

Requires `IntersectionObserver` and `requestAnimationFrame`.

## License

MIT — Free for personal and commercial use. Attribution appreciated.

---

**Inspired by** *Jujutsu Kaisen* by Gege Akutami. This is a fan project, not affiliated with MAPPA, Shueisha, or Crunchyroll.

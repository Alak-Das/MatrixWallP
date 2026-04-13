# 🕉️ Sanskrit Matrix – Dynamic Desktop Wallpaper v2.0

A Matrix-style falling-glyph live wallpaper using the **full Unicode Devanagari / Sanskrit** character set.  
Built with pure **HTML5 Canvas** — no frameworks, no dependencies — for minimal CPU/GPU usage.

---

## 📋 Character Sets (v2.0 — Full Unicode Coverage)

| Set | Unicode Range | Description |
|-----|--------------|-------------|
| Vowels | U+0904–U+0914, U+0960–U+0961 | All independent vowels incl. rare ऋ ऌ ॠ ॡ ऍ ऎ ऑ ऒ |
| Consonants | U+0915–U+0939 + nuktas | All base consonants + nukta variants क़ ख़ ग़ ज़ ड़ ढ़ फ़ य़ + ऩ ऱ ळ |
| Mātrās | U+093E–U+094D + rare | All vowel signs incl. rare ॄ ॅ ॆ ॉ ॊ ॢ ॣ, avagraha ऽ, visarga ः, anusvara ं |
| Vedic | U+0950–U+0965 | ॐ । ॥ ॰ ॱ + Vedic accent marks ॒ ॑ |
| Digits | U+0966–U+096F | Devanagari digits ० – ९ |
| Siddham / Vedic Ext. | U+1CD0–U+1CF3 | Vedic Extension combining marks |
| Extended | U+0972–U+097F, U+A8E0–U+A8F7 | Devanagari Extended block + svara marks |
| Katakana *(optional)* | U+30A2–U+30F3 | Mix of Katakana for hybrid Matrix look |

All enabled sets are drawn in **random order** — every glyph is picked uniformly at random from the combined pool each animation tick.

---

## ✨ What's New in v2.0

| # | Feature |
|---|---------|
| 1 | **Per-column speed** — each column has a random 0.6–1.4× speed multiplier for organic rainfall |
| 2 | **Comet-tail gradient** — near-head characters explicitly rendered at mid → dim → faint brightness |
| 3 | **Column density variety** — per-column bias for sparse vs dense streams, long vs short runs |
| 4 | **Ripple on click** — clicking the canvas spawns a wave of fresh streams from that point |
| 5 | **Katakana mix mode** — optional checkbox to blend Katakana with Sanskrit |
| 6 | **Density slider** — control what % of columns are active (20%–100%) |
| 7 | **Character set selectors** — individual checkboxes to enable/disable each glyph group |
| 8 | **Export / Import config** — copy/paste JSON to share or backup settings |
| 9 | **Pause / Play** — floating ⏸ button + `Space` key shortcut |
| 10 | **Google Fonts fallback** — Noto Sans Devanagari loaded from CDN if not installed locally |
| 11 | **`alpha: false` optimisation** — documented with rationale |
| 12 | **High-DPI aware** — canvas scales by `devicePixelRatio` for crisp glyphs on Retina displays |
| 13 | **Lively Wallpaper UI** — `LivelyProperties.json` exposes sliders/pickers in Lively's native panel |
| 14 | **Wallpaper Engine** — `project.json` for easy WE import |
| 15 | **Debounced resize** — 150 ms debounce prevents thrashing during window drag |
| 16 | **Cached draw constants** — COLORS, rows, speed, fadeAlpha computed once on change, not per frame |

---

## 🖥️ How to Set as Live Wallpaper

### Windows

**Option A – Lively Wallpaper (Recommended, Free & Open-Source)**
1. Download & install **Lively Wallpaper** from the Microsoft Store or  
   → https://github.com/rocksdanister/lively/releases
2. Open Lively Wallpaper.
3. Click **"+ Add Wallpaper"** → choose **"Browse"**.
4. Select `index.html` from this folder.
5. Set it as your active wallpaper.
6. *(v2.0)* Lively reads `LivelyProperties.json` and shows the settings directly in its native sidebar.

> Lively automatically pauses the animation when the desktop is hidden,  
> saving CPU when you're using other apps.

**Option B – Wallpaper Engine (Steam, Paid)**
1. Open Wallpaper Engine → **"Create Wallpaper"**.
2. Select **"Web"** type.
3. Point it to this `index.html` file.
4. The `project.json` provides metadata for the workshop.

### macOS

**Option C – Plash (Recommended, Free & Open-Source)**
macOS does not natively support web-based wallpapers, but you can set it up perfectly using Plash:
1. Download & install **Plash** from the [Mac App Store](https://apps.apple.com/app/id1494026827) or [GitHub](https://github.com/sindresorhus/Plash).
2. Open Plash (a water drop icon will appear in your menu bar).
3. Click the menu bar icon and select **"Add Local Website..."**.
4. Browse and select the `index.html` file from this folder.
5. The wallpaper will immediately start rendering as your desktop background.

### Any OS

**Option D – Preview in Browser**
Double-click `index.html` to open it in your browser and see the effect.

---

## ⚙️ Live Customization Panel

Click the **⚙** button (bottom-right, draggable) to open the settings panel.  
All settings are saved automatically to `localStorage` and persist across restarts.

| Control | Description |
|---------|-------------|
| **Color Presets** | Quick themes: Matrix, Sanskrit Gold, Cyber Cyan, Violet, Fire, Snow |
| **Head Color** | Color picker for the leading glyph — trail colors are auto-derived |
| **Background** | Background fill color |
| **Glyph Size** | 10–40 px |
| **Speed** | 0.1×–3.0× global fall speed (per-column variation is always on) |
| **Trail Length** | Very Long → Instant |
| **FPS Cap** | 6–60 fps |
| **Density** | 20%–100% active columns |
| **Character Sets** | Vowels / Consonants / Mātrās / Vedic / Digits / Siddham / Extended / Katakana |
| **Export / Import** | Share or restore settings as JSON |
| **⏸ Pause** | Freeze animation (also: `Space` key) |
| **↺ Reset** | Restore all settings to defaults |

---

## 💡 Resource Usage Tips

| Setting | Lower CPU | Effect |
|---------|-----------|--------|
| `FPS Cap` | Reduce to 12–15 | Smoother for high-res screens |
| `Glyph Size` | Increase to 22–28 | Fewer columns = less work |
| `Density` | Reduce to 60–80% | Fewer active columns |
| `Trail Length` | Increase (shorter trail) | Fewer pixels repainted |

---

## 🔤 Font

The wallpaper uses: `"Noto Sans Devanagari"`, `"Mangal"`, falling back to monospace.  
**v2.0** also preloads **Noto Sans Devanagari** directly from Google Fonts as a CDN fallback.  
Install locally for best results: https://fonts.google.com/noto/specimen/Noto+Sans+Devanagari

---

*Made with ❤️ and ॐ by Alak D*

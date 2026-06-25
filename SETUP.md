# Setup Guide — Danyal Ahmad's Profile README (Unique Edition v2)

This zip contains a unique, bold GitHub profile README using **LinkedIn blue (`#0a66c2`)** + **acid yellow (`#e8fa03`)** on pure black, with morph banners, ASCII signature, year progress bars, "Now" status terminal, shark dividers, and 9 typing animations.

## 1. Push to your PROFILE repo

The `README.md` must live in a repo named **exactly after your username**: `Danyal-Ahmad/Danyal-Ahmad`.

```
Danyal-Ahmad/
├── README.md
├── github-metrics.svg           ← placeholder; replaced by metrics.yml
├── SETUP.md
└── .github/
    └── workflows/
        ├── snake.yml              ← snake animation (visible in § 04)
        ├── metrics.yml            ← metrics SVG (visible in § 03)
        └── profile-3d.yml         ← 3D contribution calendar (visible in § 04)
```

## 2. Create one secret

The `metrics.yml` workflow needs a Personal Access Token:

1. **GitHub → Settings → Developer settings → Personal access tokens → Fine-grained tokens**
2. Generate a token scoped to `Danyal-Ahmad/Danyal-Ahmad` with **Contents: Read and write** + **Metadata: Read-only**
3. **Repo → Settings → Secrets and variables → Actions → New repository secret**
4. Name it `METRICS_TOKEN`, paste the token

The other workflows use the built-in `GITHUB_TOKEN`.

## 3. Trigger each workflow once

Go to **Actions → Run workflow** for each:

| Workflow | Output | Visible in README? |
|---|---|---|
| `Generate Snake Animation` | `output` branch | ✅ Yes — `§ 04` |
| `GitHub Profile 3D Contribution` | `output-3d-contrib` branch | ✅ Yes — `§ 04` |
| `Metrics` | commits `github-metrics.svg` to `main` | ✅ Yes — `§ 03` |

## 4. README sections (9 sections + "Now" widget)

| # | Section | Status |
|---|---|---|
| (top) | NOW widget — live status terminal (researching, building, reading, listening + focus metrics) | ✅ Real content |
| `01 ·` | About — 2-paragraph bio + typing header | ✅ Real content |
| `02 ·` | Stack — left-aligned stacked layout, 4 categories | ✅ Real |
| `03 ·` | Metrics — 2x2 grid + activity graph + detailed dashboard | ✅ Live |
| `04 ·` | Contribution Atlas — snake + 3D calendar | ✅ Live |
| `05 ·` | Currently Building — 3 paragraphs | ✅ Real content |
| `06 ·` | What I'm Learning — left-aligned, This Week + On The Radar | ✅ Real content |
| `07 ·` | Philosophy — 5 bullets | ✅ Real content |
| `08 ·` | Quote — LIVE widget | ✅ Live |
| `09 ·` | Connect — GitHub · LinkedIn · Email | ✅ Real |

## 5. Design system — Blue + Yellow on Black

- **Background**: Pure black `#0A0A0A`
- **Primary accent**: LinkedIn blue `#0A66C2`
- **Secondary accent**: Acid yellow `#E8FA03`
- **Text**: Pure white `#FFFFFF`
- **Morph banners**: `capsule-render venom` (top: solid yellow with black username; bottom: solid blue with white text)
- **Shark dividers**: `capsule-render shark` type — organic, animated, alternating blue/yellow between sections
- **Left-aligned stack**: Stack and Learning sections use `align="left"` for editorial feel
- **Multiple typing animations**: 9 total — one per section, alternating blue/yellow

## 6. NEW unique UI elements in this version

| Element | Description |
|---|---|
| **ASCII signature** | Block-style ASCII art of "DANYAL AHMAD" below the top banner — pure typographic identity, no image |
| **Year progress bars** | Two real-time progress bars: `2026 → 50%` (blue) and `CS Degree → 50%` (yellow), powered by `progress-bar.xyz` |
| **NOW widget** | Two-column status terminal at the top showing what you're currently researching/building/reading/listening + focus metrics (recall@5, inference time, models in prod, projects shipped) |
| **Shark dividers** | `capsule-render shark` type between every section — alternating blue and yellow, organic undulating shape, much more unique than flat rect dividers |
| **2x2 metrics grid** | Stats · Top Languages · Streak · Trophies arranged in a 2x2 grid for visual balance (was stacked vertically) |
| **Trophies widget** | Added `github-profile-trophy` to the metrics grid — animated rank tiles |
| **Better metrics placeholder** | The `github-metrics.svg` placeholder is now 900x320 natively (was 480x120) — looks like a real dashboard with avatar, name, stats grid, and animated language bars. Doesn't stretch weirdly when displayed at `width="100%"` |

## 7. Color usage map

| Section | Typing color | Accent color |
|---|---|---|
| Banner (top) | — | Yellow (solid) + black username |
| ASCII signature | — | White on black |
| Year progress | — | Blue (2026) + Yellow (degree) |
| Header typing | Blue | Yellow (subtitle) |
| NOW widget | — | Blue + Yellow labels |
| Shark divider 1 | — | Blue |
| `01 · About` | Blue | — |
| Shark divider 2 | — | Yellow |
| `02 · Stack` | Yellow | Alternating blue/yellow labels |
| Shark divider 3 | — | Blue |
| `03 · Metrics` | Blue | Blue titles + yellow icons/streak + trophies |
| Shark divider 4 | — | Yellow |
| `04 · Atlas` | Yellow | — |
| Shark divider 5 | — | Blue |
| `05 · Building` | Blue | — |
| Shark divider 6 | — | Yellow |
| `06 · Learning` | — | Yellow (This Week) + Blue (On Radar) |
| Shark divider 7 | — | Blue |
| `07 · Philosophy` | Yellow | — |
| Shark divider 8 | — | Yellow |
| `08 · Quote` | — | Blue border |
| Shark divider 9 | — | Blue |
| `09 · Connect` | Blue | Blue (GitHub/LinkedIn) + Yellow (Email) |
| Banner (bottom) | — | Blue (solid) + white text |

## 8. External resources used

| Resource | What it does |
|---|---|
| **capsule-render** | `venom` banners (top + bottom) + `shark` dividers (9 between sections) |
| **readme-typing-svg** | 9 typing animations throughout |
| **progress-bar.xyz** | Year + degree progress bars (NEW) |
| **shields.io** | Status pills, social badges, section labels |
| **skillicons.dev** | Tech stack icons |
| **komarev** | Profile view counter |
| **github-readme-stats** | Stats card + top languages |
| **github-profile-trophy** | Animated trophy rank tiles (NEW) |
| **streak-stats** | GitHub streak |
| **github-readme-activity-graph** | Contribution activity graph |
| **quotes-github-readme** | Live random dev quote |
| **Platane/snk** | Snake animation (via workflow) |
| **yoshi389111/github-profile-3d-contrib** | 3D contribution calendar (via workflow) |
| **lowlighter/metrics** | Detailed metrics dashboard (via workflow) |

## 9. What changed in this version (Unique Edition v2)

**Metrics field FIXED:**
- ❌ Old placeholder: 480x120 SVG, displayed at `width="100%"` → stretched and broken
- ✅ New placeholder: **900x320 SVG** with realistic dashboard layout (header bar, avatar, name, 4-stat grid, animated language bars) — displays naturally at any width

**UI made more unique:**
- ✨ Added **ASCII signature** of "DANYAL AHMAD" — pure typographic identity, no image
- ✨ Added **2 year progress bars** (2026 + CS Degree) at the top — real-time, dynamic
- ✨ Added **NOW widget** — two-column live status terminal showing current research/build/read/listen + focus metrics
- ✨ Replaced flat `rect` dividers with **`shark` dividers** — 9 organic animated dividers alternating blue/yellow
- ✨ Redesigned metrics section as **2x2 grid** (Stats · Top Langs · Streak · Trophies) instead of vertical stack
- ✨ Added **github-profile-trophy** widget to the metrics grid
- ✨ Shark dividers create a unique visual rhythm — sections now feel like waves flowing down the page

---

Stay curious · Ship often · Document everything.

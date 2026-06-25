# Setup Guide — Danyal Ahmad's Profile README (Monochrome Edition)

This zip contains a clean, minimal, monochrome (black & white) GitHub profile README with morph/venom animated banners and editorial typography.

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
        ├── metrics.yml            ← general metrics SVG (committed to main)
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
| `Metrics` | commits `github-metrics.svg` to `main` | No (kept for reference) |

## 4. README sections (9 sections, all working)

| # | Section | Status |
|---|---|---|
| `01 ·` | About — 2-paragraph bio | ✅ Real content |
| `02 ·` | Stack — skillicons only, 4 rows | ✅ Real |
| `03 ·` | Metrics — 2 cards + activity graph | ✅ Live |
| `04 ·` | Contribution Atlas — snake + 3D calendar | ✅ Live |
| `05 ·` | Currently Building — 3 paragraphs | ✅ Real content |
| `06 ·` | What I'm Learning — table | ✅ Real content |
| `07 ·` | Philosophy — 5 bullets | ✅ Real content |
| `08 ·` | Quote — LIVE widget (no workflow) | ✅ Live |
| `09 ·` | Connect — GitHub · LinkedIn · Email | ✅ Real |

## 5. Design system — Monochrome

- **Aesthetic**: Pure black (`#0A0A0A`) + pure white (`#FFFFFF`) + grey (`#A9A9A9`)
- **No color anywhere** — all widgets use `theme=white` + `bg_color=0A0A0A` + `text_color=FFFFFF`
- **Section markers**: `01 ·` through `09 ·` (editorial style)
- **No emoji** — clean editorial typography
- **Morph banners**: `capsule-render venom` type at top and bottom (organic, animated)
- **Hairline dividers**: `andreasbm/readme` colored lines (subtle)
- **Square corners** (`border_radius=0`) — sharp, editorial, minimal
- **Live widgets**: All dynamic content uses real GitHub data — no fake SVGs

## 6. External resources used

| Resource | What it does | URL |
|---|---|---|
| **capsule-render** | Morph/venom animated banners (top + bottom) | `capsule-render.vercel.app` |
| **readme-typing-svg** | Animated typing headline | `readme-typing-svg.demolab.com` |
| **shields.io** | Status pills, social badges | `img.shields.io` |
| **skillicons.dev** | Tech stack icons | `skillicons.dev` |
| **komarev** | Profile view counter | `komarev.com/ghpvc` |
| **github-readme-stats** | Stats card + top languages | `github-readme-stats.vercel.app` |
| **github-readme-activity-graph** | Contribution activity graph | `github-readme-activity-graph.vercel.app` |
| **quotes-github-readme** | Live random dev quote | `quotes-github-readme.vercel.app` |
| **andreasbm/readme** | Hairline dividers | `raw.githubusercontent.com/andreasbm/readme` |
| **Platane/snk** | Snake animation (via workflow) | `github.com/Platane/snk` |
| **yoshi389111/github-profile-3d-contrib** | 3D contribution calendar (via workflow) | `github.com/yoshi389111/github-profile-3d-contrib` |
| **lowlighter/metrics** | Detailed metrics SVG (via workflow) | `github.com/lowlighter/metrics` |

## 7. What changed in this version (Monochrome Edition)

**Aesthetic overhaul:**
- ✨ Switched from electric cyan to **pure black & white** — no color anywhere
- ✨ New **morph/venom animated banners** (top + bottom) via capsule-render — organic, undulating shapes
- ✨ **Hairline dividers** between sections (subtle, editorial)
- ✨ **Square corners** on all cards (`border_radius=0`) — sharp, minimal
- ✨ Removed all emojis — clean editorial typography only
- ✨ Removed profile summary card, sticker row, status pills row (kept only 4 essential pills)
- ✨ Section markers simplified from `// 01` to `01 ·` (cleaner editorial style)

**Reduced visual noise:**
- GitHub Stats reduced to 2 cards (stats + top langs) + 1 activity graph
- Removed detailed metrics card, classic contribution chart, language SVG from the visible README
- Only 1 quote widget (no jokes, no extra widgets)

**Workflows cleaned up:**
- Kept 3 essential workflows: snake, metrics, profile-3d
- Removed: activity, metrics-languages (not used in visible README)

## 8. Everything is REAL

Every dynamic widget points at `username=Danyal-Ahmad`:
- Stats, top langs, activity graph → live from GitHub API
- Snake + 3D calendar → live, eating your real contribution grid
- Visit counter → increments per unique visitor (komarev)
- Quote → live random quote (refreshes on each render)

---

Stay curious · Ship often · Document everything.

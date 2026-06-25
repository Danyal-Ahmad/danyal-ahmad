# Setup Guide — Danyal Ahmad's Profile README (Editorial Brutalist Edition)

A clean, editorial, brutalist GitHub profile README. Pure black with LinkedIn blue (`#0a66c2`) + acid yellow (`#e8fa03`). Real data throughout — no fake placeholders.

## 1. Push to your PROFILE repo

The `README.md` must live in a repo named **exactly after your username**: `Danyal-Ahmad/Danyal-Ahmad`.

```
Danyal-Ahmad/
├── README.md
├── github-metrics.svg           ← REAL static dashboard (data baked in)
├── SETUP.md
└── .github/
    └── workflows/
        ├── snake.yml              ← snake animation
        ├── metrics.yml            ← refreshes github-metrics.svg daily
        └── profile-3d.yml         ← 3D contribution calendar
```

## 2. The github-metrics.svg is REAL — not a placeholder

Unlike previous versions that shipped a "loading…" placeholder, this zip includes a **fully-realized static SVG dashboard** with your actual GitHub data baked in:

- **Identity block**: avatar (DA initials), name "Danyal Ahmaad", handle @Danyal-Ahmad, role "AI · ML Engineer · Lahore, Pakistan"
- **Account meta**: Joined Dec 2020, last active 2026, ● Hireable
- **Real bio**: Pulled verbatim from your GitHub profile
- **Stats grid**: 4 public repos · 2 followers · 1 following · 1 star earned (all real)
- **Language breakdown bar**: TypeScript 40% · JavaScript 30% · CSS 20% · PHP 10% (computed from your real public repos)
- **Color-coded language legend** with percentages

This SVG renders correctly the moment you push the repo — no workflow run required. Once you run the `Metrics` workflow, it gets overwritten by `lowlighter/metrics`'s auto-generated version with the same data but live-refreshed.

## 3. Create one secret

The `metrics.yml` workflow needs a Personal Access Token:

1. **GitHub → Settings → Developer settings → Personal access tokens → Fine-grained tokens**
2. Generate a token scoped to `Danyal-Ahmad/Danyal-Ahmad` with **Contents: Read and write** + **Metadata: Read-only**
3. **Repo → Settings → Secrets and variables → Actions → New repository secret**
4. Name it `METRICS_TOKEN`, paste the token

The other two workflows use the built-in `GITHUB_TOKEN`.

## 4. Trigger each workflow once

Go to **Actions → Run workflow** for each:

| Workflow | Output | Visible in README? |
|---|---|---|
| `Generate Snake Animation` | `output` branch | ✅ Yes — `§ 04` |
| `GitHub Profile 3D Contribution` | `output-3d-contrib` branch | ✅ Yes — `§ 04` |
| `Metrics` | commits `github-metrics.svg` to `main` | ✅ Yes — `§ 03` (overwrites the static version) |

## 5. README sections (9 sections, all working)

| # | Section | Status |
|---|---|---|
| `01 /` | Identity — 2-paragraph bio | ✅ Real content |
| `02 /` | Stack — left-aligned, 4 categories | ✅ Real |
| `03 /` | Signal — REAL dashboard SVG + live stats + activity graph | ✅ Live |
| `04 /` | Contribution Atlas — snake + 3D calendar | ✅ Live |
| `05 /` | Currently Building — 3 paragraphs | ✅ Real content |
| `06 /` | What I'm Learning — This Week + On The Radar | ✅ Real content |
| `07 /` | Philosophy — 5 bullets | ✅ Real content |
| `08 /` | Quote — LIVE widget | ✅ Live |
| `09 /` | Connect — GitHub · LinkedIn · Email | ✅ Real |

## 6. What was stripped out (per request — "too overrated")

- ❌ ASCII art signature
- ❌ Shark dividers (capsule-render shark)
- ❌ Year progress bars (progress-bar.xyz)
- ❌ NOW widget with emojis
- ❌ Trophies widget (github-profile-trophy)
- ❌ 9 typing animations (reduced to 1)
- ❌ Capsule-render venom banners (top + bottom)
- ❌ Streak stats widget
- ❌ Multiple status pills rows
- ❌ Emoji section icons
- ❌ "Loading…" placeholder SVG

## 7. What replaced them (real identity, not decoration)

- ✅ **Plain H1 name** — "DANYAL AHMAD" in GitHub's native heading style, left-aligned
- ✅ **Single typing animation** — three lines of real philosophy, not 9 different ones
- ✅ **`<hr>` dividers** — clean horizontal rules between sections
- ✅ **`01 /` section markers** — slash separator (more editorial than `01 ·`)
- ✅ **REAL static metrics SVG** — actual dashboard with real data, not a placeholder
- ✅ **Left-aligned layout** — editorial / brutalist, not centered
- ✅ **Plain bold text** for stack category labels (not colored badges)
- ✅ **Plain bullets** for learning section (not code-styled chips)
- ✅ **Minimal status pills** — only 4, all in a single row

## 8. Design system

- **Background**: Pure black `#0A0A0A`
- **Primary accent**: LinkedIn blue `#0A66C2`
- **Secondary accent**: Acid yellow `#E8FA03`
- **Text**: Pure white `#FFFFFF`
- **Muted text**: `#A9A9A9`
- **Dividers**: Native GitHub `<hr>` (no capsule-render)
- **Layout**: Left-aligned throughout (not centered)
- **Section markers**: `01 /` through `09 /` (editorial slash style)
- **Typography**: GitHub native (system sans for body, monospace for code/typing)

## 9. External resources used (minimal, only what's needed)

| Resource | What it does |
|---|---|
| **readme-typing-svg** | 1 typing animation (header) |
| **shields.io** | 4 status pills + 3 social badges |
| **skillicons.dev** | Tech stack icons |
| **komarev** | Profile view counter |
| **github-readme-stats** | Stats card + top languages |
| **github-readme-activity-graph** | Contribution activity graph |
| **quotes-github-readme** | Live random dev quote |
| **Platane/snk** | Snake animation (via workflow) |
| **yoshi389111/github-profile-3d-contrib** | 3D contribution calendar (via workflow) |
| **lowlighter/metrics** | Refreshes the static SVG daily (via workflow) |

---

Stay curious · Ship often · Document everything.

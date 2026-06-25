# Setup Guide — Danyal Ahmad's Profile README (Blue + Yellow Edition)

This zip contains a unique, bold GitHub profile README using **LinkedIn blue (`#0a66c2`)** + **acid yellow (`#e8fa03`)** on pure black, with morph banners, multiple typing animations, and a stacked (non-table) layout.

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

## 4. README sections (9 sections, all working)

| # | Section | Status |
|---|---|---|
| `01 ·` | About — 2-paragraph bio + typing header | ✅ Real content |
| `02 ·` | Stack — stacked layout (NOT a table), 4 categories | ✅ Real |
| `03 ·` | Metrics — stats + top langs + streak + activity graph + detailed dashboard | ✅ Live |
| `04 ·` | Contribution Atlas — snake + 3D calendar | ✅ Live |
| `05 ·` | Currently Building — 3 paragraphs | ✅ Real content |
| `06 ·` | What I'm Learning — stacked badges + text | ✅ Real content |
| `07 ·` | Philosophy — 5 bullets | ✅ Real content |
| `08 ·` | Quote — LIVE widget | ✅ Live |
| `09 ·` | Connect — GitHub · LinkedIn · Email | ✅ Real |

## 5. Design system — Blue + Yellow on Black

- **Background**: Pure black `#0A0A0A`
- **Primary accent**: LinkedIn blue `#0A66C2`
- **Secondary accent**: Acid yellow `#E8FA03`
- **Text**: Pure white `#FFFFFF`
- **Morph banners**: `capsule-render venom` type (top + bottom) with blue → black → yellow gradient
- **Hairline dividers**: `capsule-render rect` (blue at top, yellow at bottom)
- **Stacked layout**: Stack section uses centered badges + skillicons — NOT a 2-column table
- **Multiple typing animations**: 9 total — one per section, alternating blue/yellow

## 6. Color usage map

| Section | Typing color | Accent color |
|---|---|---|
| Header (top) | Blue `#0A66C2` | Yellow `#E8FA03` (subtitle) |
| `01 · About` | Blue | — |
| `02 · Stack` | Yellow | Alternating blue/yellow labels |
| `03 · Metrics` | Blue | Blue titles + yellow icons/streak |
| `04 · Atlas` | Yellow | — |
| `05 · Building` | Blue | — |
| `06 · Learning` | — | Yellow (Deepening) + Blue (Exploring) |
| `07 · Philosophy` | Yellow | — |
| `08 · Quote` | — | Blue border |
| `09 · Connect` | Blue | Blue (GitHub/LinkedIn) + Yellow (Email) |
| Footer (bottom) | — | Blue → Black → Yellow gradient |

## 7. External resources used

| Resource | What it does |
|---|---|
| **capsule-render** | Morph/venom banners (top + bottom) + rect dividers |
| **readme-typing-svg** | 9 typing animations throughout |
| **shields.io** | Status pills, social badges, section labels |
| **skillicons.dev** | Tech stack icons |
| **komarev** | Profile view counter |
| **github-readme-stats** | Stats card + top languages |
| **streak-stats** | GitHub streak |
| **github-readme-activity-graph** | Contribution activity graph |
| **quotes-github-readme** | Live random dev quote |
| **Platane/snk** | Snake animation (via workflow) |
| **yoshi389111/github-profile-3d-contrib** | 3D contribution calendar (via workflow) |
| **lowlighter/metrics** | Detailed metrics dashboard (via workflow) |

## 8. What changed in this version (Blue + Yellow Edition)

**Theme switched:**
- ❌ Old: Pure black & white monochrome
- ✅ New: **LinkedIn blue (`#0A66C2`) + acid yellow (`#E8FA03`)** on pure black

**Stack section redesigned (per request):**
- ❌ Old: 2-column table (label column + icons column)
- ✅ New: **Stacked centered layout** — each category is a colored badge, followed by its skillicons row, with vertical spacing between categories

**Stats properly arranged (per request):**
- ❌ Old: 2 cards in a table + activity graph
- ✅ New: **5 widgets stacked vertically** — stats card → top languages → streak stats → activity graph → detailed metrics dashboard. Each gets full width and proper breathing room.

**More typing animations (per request):**
- ❌ Old: 2 typing animations (header + subtitle)
- ✅ New: **9 typing animations** — one per section, alternating blue/yellow. Examples: `> whoami?`, `> $ stack --list`, `> $ git stats --live`, `> eating my contribution grid...`, `> git commit -m "building..."`, `> cat philosophy.md`, `> let's build together`

**Color theming applied to all live widgets:**
- Stats card: blue title, yellow icons
- Top Languages: blue title
- Streak stats: blue ring, yellow fire/labels
- Activity graph: blue line, yellow points
- Quote widget: blue border
- Visit counter: blue accent

---

AI / ML Engineer · CS Undergrad · Lahore, Pakistan

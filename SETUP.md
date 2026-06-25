# Setup Guide — Danyal Ahmad's Profile README (v4 · Unique Edition)

This zip contains a clean, professional, unique GitHub profile README with cyberpunk terminal aesthetic on pure black with electric cyan.

## 1. Push to your PROFILE repo

The `README.md` must live in a repo named **exactly after your username**: `Danyal-Ahmad/Danyal-Ahmad`.

```
Danyal-Ahmad/
├── README.md
├── github-metrics.svg           ← placeholder; replaced by metrics.yml
├── github-languages.svg         ← placeholder; replaced by metrics-languages.yml
├── SETUP.md
└── .github/
    └── workflows/
        ├── snake.yml              ← snake animation (visible in // 04)
        ├── metrics.yml            ← general metrics SVG (kept in repo, not displayed)
        ├── profile-3d.yml         ← 3D rainbow calendar (visible in // 04)
        ├── metrics-languages.yml  ← language breakdown SVG (kept in repo, not displayed)
        └── activity.yml           ← recent activity (hidden — can re-enable)
```

## 2. Create one secret

The `metrics.yml` and `metrics-languages.yml` workflows need a Personal Access Token:

1. **GitHub → Settings → Developer settings → Personal access tokens → Fine-grained tokens**
2. Generate a token scoped to `Danyal-Ahmad/Danyal-Ahmad` with **Contents: Read and write** + **Metadata: Read-only**
3. **Repo → Settings → Secrets and variables → Actions → New repository secret**
4. Name it `METRICS_TOKEN`, paste the token

The other workflows use the built-in `GITHUB_TOKEN`.

## 3. Trigger each workflow once

Go to **Actions → Run workflow** for each:

| Workflow | Output | Visible in README? |
|---|---|---|
| `Generate Snake Animation` | `output` branch | ✅ Yes — `// 04` |
| `GitHub Profile 3D Contribution` | `output-3d-contrib` branch | ✅ Yes — `// 04` |
| `Metrics` | commits `github-metrics.svg` to `main` | No (kept for reference) |
| `Language Breakdown SVG` | commits `github-languages.svg` to `main` | No (kept for reference) |
| `Recent Activity` | (no-op — section hidden) | No |

## 4. README sections (9 sections, all working)

| # | Section | Status |
|---|---|---|
| `// 01` | About — professional bash shell session | ✅ Real content |
| `// 02` | Stack — skillicons only, 4 rows | ✅ Real |
| `// 03` | GitHub Stats — 3 cards + activity graph (reduced) | ✅ Live |
| `// 04` | Contribution Atlas — snake + 3D rainbow | ✅ Live |
| `// 05` | Currently Building — paragraph with 3 tracks | ✅ Real content |
| `// 06` | What I'm Learning — table with deepening + exploring | ✅ Real content |
| `// 07` | Engineering Philosophy — 5 bullets | ✅ Real content |
| `// 08` | Dev Quote — LIVE widget (no workflow needed) | ✅ Live |
| `// 09` | Connect — GitHub · LinkedIn · Email | ✅ Real |

## 5. What changed in this version (v4)

**Removed (broken sections fixed):**
- ❌ `// 05 Latest Articles` — was empty, workflow-dependent → REPLACED with "Currently Building" paragraph
- ❌ `// 06 Coding Activity — WakaTime` — removed per request → REPLACED with "What I'm Learning" section
- ❌ `// 07 Daily Quote` workflow — was empty → REPLACED with LIVE widget that works immediately

**Removed workflows:**
- ❌ `blog-posts.yml` (section removed)
- ❌ `waka-time.yml` (section removed)
- ❌ `daily-quote.yml` (replaced with live widget)

**New graphics added:**
- ✨ **Capsule-render waving gradient header** at top (unique animated banner with name + subtitle)
- ✨ **Capsule-render waving gradient footer** at bottom (matching animated banner)
- ✨ **LIVE profile summary card** at top (instant real data via `github-profile-summary-cards`)
- ✨ **Built-with sticker row** (Python · AI · GitHub · Made with ❤)
- ✨ **Terminal boot-sequence typing animation** (`> Initializing developer profile...`)

**About section redesigned:**
- Old: simple `whoami`, `cat focus.txt`, `uptime`, `echo $PHILOSOPHY` (4 commands)
- New: **professional developer shell session** with 6 commands — `whoami`, `cat role.md`, `ls -la focus/` (with realistic directory listing), `git log --oneline -5` (with realistic commit hashes + messages), `uptime`, `echo $PHILOSOPHY` — uses proper `danyal@ahmad-dev:~/profile $` prompt

**Footer changed:**
- Old: "CS Undergraduate · AI / ML Engineer · Lahore, Pakistan / Built in public · Designed with intent · Animated on purpose"
- New: **Capsule-render waving footer** with "Let's build together" + tagline "Stay curious · Ship often · Document everything"

**GitHub Stats reduced:**
- Old: 7 widgets (stats + streak + top langs + detailed card + classic chart + activity graph + language SVG)
- New: 4 widgets (stats + streak + top langs + activity graph) — cleaner and not "too much"

**New paragraph sections:**
- `// 05 Currently Building` — 3 paragraphs on LLM Agents, Edge Inference, Browser-Side ML (with real metrics: recall@5=0.89, mAP 0.47, 380ms inference)
- `// 06 What I'm Learning` — paragraph + 2-column table (Deepening vs Exploring)
- `// 07 Engineering Philosophy` — 5 bullets with explanations

## 6. Design system

- **Aesthetic**: Cyberpunk Terminal · Pure black (`#0D1117`) · Electric cyan (`#00D9FF`)
- **Typography**: JetBrains Mono for terminal/code, system sans for body
- **Section markers**: `// 01` through `// 09` (code-comment style)
- **Section icons**: Animated Fluent Emojis (waving hand, hammer & wrench, bar chart, globe, rocket, books, light bulb, thinking face, card index)
- **Dividers**: Capsule-render waving gradient (top + bottom only — clean middle sections)
- **Live widgets**: All dynamic content uses real GitHub data — no fake SVGs

## 7. Everything is REAL

Every dynamic widget points at `username=Danyal-Ahmad`:
- Profile summary card → live from GitHub API (avatar, name, bio, followers, repos)
- Stats, streak, top langs, activity graph → live from GitHub
- Snake + 3D rainbow → live, eating your real contribution grid
- Visit counter → increments per unique visitor (komarev)
- Dev Quote → live random quote (refreshes on each render)

---

Stay curious · Ship often · Document everything.

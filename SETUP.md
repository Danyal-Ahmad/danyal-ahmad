# Setup Guide — Danyal Ahmad's Profile README (Extended Edition)

This zip contains everything you need to make your GitHub profile README fully alive — **8 workflows**, 4 new auto-updating sections, real data throughout, cyberpunk terminal aesthetic on pure black with electric cyan.

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
        ├── snake.yml              ← snake animation
        ├── metrics.yml            ← general metrics dashboard
        ├── profile-3d.yml         ← 3D rainbow calendar
        ├── activity.yml           ← recent activity (hidden, kept for re-enable)
        ├── blog-posts.yml         ← NEW: RSS auto-pull into README
        ├── waka-time.yml          ← NEW: WakaTime coding stats
        ├── daily-quote.yml        ← NEW: daily dev quote auto-update
        └── metrics-languages.yml  ← NEW: detailed language breakdown SVG
```

## 2. Create repo secrets

### Required (1 secret)
| Secret name | Where to get it |
|---|---|
| `METRICS_TOKEN` | GitHub → Settings → Developer settings → Personal access tokens → Fine-grained tokens. Scope to `Danyal-Ahmad/Danyal-Ahmad` with **Contents: Read and write** + **Metadata: Read-only**. |

### Optional (1 secret — enables // 06 Coding Activity)
| Secret name | Where to get it |
|---|---|
| `WAKATIME_API_KEY` | Sign up at https://wakatime.com (free), install the editor plugin, then copy your API key from https://wakatime.com/settings/account |

The other 6 workflows use the built-in `GITHUB_TOKEN` — no setup needed.

## 3. Trigger each workflow once

Go to **Actions → Run workflow** for each:

| Workflow | Output | Secret needed? |
|---|---|---|
| `Generate Snake Animation` | `output` branch | — |
| `GitHub Profile 3D Contribution` | `output-3d-contrib` branch | — |
| `Metrics` | commits `github-metrics.svg` to `main` | `METRICS_TOKEN` |
| `Language Breakdown SVG` | commits `github-languages.svg` to `main` | `METRICS_TOKEN` |
| `Latest Blog Posts` | fills `<!--START_SECTION:blog-posts-->` in `main` | — |
| `WakaTime Coding Stats` | fills `<!--START_SECTION:waka-->` in `main` | `WAKATIME_API_KEY` |
| `Daily Dev Quote` | fills `<!--START_SECTION:quote-->` in `main` | — |
| `Recent Activity` | (no-op — section hidden, can re-enable) | — |

After the first manual run, everything auto-updates on its schedule (hourly / daily).

## 4. README sections (extended to 8)

| # | Section | Live? |
|---|---|---|
| `// 01` | About — CS undergrad, Lahore, AI/ML focus | ✅ Real content |
| `// 02` | Stack — skillicons only, 4 rows | ✅ Real |
| `// 03` | GitHub Stats — extended (stats + streak + top langs + detailed card + classic chart + activity graph + language SVG) | ✅ Live |
| `// 04` | Contribution Atlas — snake + 3D rainbow | ✅ Live |
| `// 05` | Latest Articles — RSS auto-pull | ✅ Auto-updated |
| `// 06` | Coding Activity — WakaTime | ✅ Auto-updated (needs WAKATIME_API_KEY) |
| `// 07` | Daily Quote — auto-updated | ✅ Auto-updated |
| `// 08` | Connect — GitHub · LinkedIn · Email | ✅ Real |

## 5. Customizing the RSS feed (// 05 Latest Articles)

By default, `blog-posts.yml` pulls from `https://dev.to/feed/` (dev.to's global featured feed). To pull your own content:

1. Find your RSS URL — examples:
   - **YouTube channel**: `https://www.youtube.com/feeds/videos.xml?channel_id=UCxxxxxxxx` (find channel ID at https://commentpicker.com/youtube-channel-id.php)
   - **Dev.to**: `https://dev.to/feed/username`
   - **Medium**: `https://medium.com/feed/@username`
   - **Personal blog**: most platforms expose `/feed`, `/rss`, or `/atom.xml`
2. Edit `.github/workflows/blog-posts.yml` and replace the `feed_list` value.
3. The workflow will pick up the change on the next push.

You can list multiple feeds separated by commas:
```yaml
feed_list: "https://dev.to/feed/danyal,https://www.youtube.com/feeds/videos.xml?channel_id=UCxxxx"
```

## 6. Design notes

- **Aesthetic**: Cyberpunk Terminal · Pure black (`#0D1117`) · Electric cyan (`#00D9FF`)
- **8 workflows** total — 4 existing + 4 NEW
- **New visit counter**: switched from getloli to **komarev profile-views** (`https://komarev.com/ghpvc/?username=Danyal-Ahmad`) — cleaner, more professional, no anime theme
- **Removed sections**: `// 03 Featured Work` and `// 06 Recent Activity` per request
- **New sections added**: Latest Articles, Coding Activity, Daily Quote
- **Extended GitHub Stats**: now 5 widgets stacked — stats card · streak · top langs · detailed metrics card (issues/PRs/reviews) · classic contribution chart · activity graph · language SVG
- **Terminal aesthetic**: `$ whoami`, `$ cat focus.txt`, `$ uptime`, `$ echo $PHILOSOPHY` code block in About section
- **Live status pills**: STATUS-Online, BUILDING-Intelligent_Systems, SHIPPING-End_to_End

## 7. What's REAL

Every dynamic widget points at `username=Danyal-Ahmad`:
- Stats, streak, top langs, activity graph → live from GitHub API
- Classic contribution chart (`ghchart.rshah.org`) → live from GitHub
- Snake + 3D rainbow → live, eating your real contribution grid
- Visit counter → increments per unique visitor (komarev)
- Latest articles → real RSS feed (defaults to dev.to, swap your own)
- WakaTime → your real coding hours (once API key is added)
- Daily quote → real auto-updated quote

---

Built in public · Designed with intent · Animated on purpose.

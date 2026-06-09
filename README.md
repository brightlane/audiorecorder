# AudioRecorder Affiliate Site — build.py v1

Independent affiliate marketing website for [Wondershare Streaming Audio Recorder](https://videoconverter.wondershare.com), built for GitHub Pages at:

**`https://brightlane.github.io/audiorecorder/`**

---

## Quick Start

```bash
python3 build.py
```

Outputs 47 files into `audiorecorder-site/` next to `build.py`. Zero dependencies — pure Python 3 stdlib only.

---

## Deployment

Your repo needs exactly three files:

```
audiorecorder/                  ← your GitHub repo name
├── build.py
├── README.md
└── .github/
    └── workflows/
        └── deploy.yml
```

**One-time GitHub setup:**
1. `Settings → Pages → Source` → set to **GitHub Actions**
2. Push to `main` — workflow builds and deploys in ~30 seconds

---

## Config (top of build.py)

```python
BASE      = Path(__file__).parent / "audiorecorder-site"
SITE_ROOT = "/audiorecorder"                    # Must match repo name exactly
SITE_URL  = "https://brightlane.github.io/audiorecorder"
AFF       = "https://www.linkconnector.com/ta.php?lc=007949049070004532&atid=audiorecorderwebs"
YEAR      = date.today().year
```

⚠️ `SITE_ROOT` must match your GitHub repo name exactly or all links will 404.

---

## All 21 Pages

| Page | URL | Schema |
|---|---|---|
| Homepage | `/` | SoftwareApp + Breadcrumb |
| Features | `/features/` | SoftwareApp + ItemList |
| How It Works | `/how-it-works/` | SoftwareApp + HowTo |
| Use Cases | `/use-cases/` | SoftwareApp + Breadcrumb |
| Formats | `/formats/` | SoftwareApp + Breadcrumb |
| Pricing | `/pricing/` | SoftwareApp + FAQPage |
| Review | `/review/` | SoftwareApp + Review |
| FAQ | `/faq/` | SoftwareApp + FAQPage |
| Download | `/download/` | SoftwareApp + Breadcrumb |
| Blog | `/blog/` | SoftwareApp + Breadcrumb |
| Record Streaming Audio | `/record-streaming-audio/` | SoftwareApp + HowTo + Article |
| Record Zoom Audio | `/record-zoom-audio/` | SoftwareApp + Article |
| Record Spotify | `/record-spotify/` | SoftwareApp + Article |
| Podcast Recorder | `/podcast-recorder/` | SoftwareApp + Article |
| Voice Recorder | `/voice-recorder/` | SoftwareApp + Article |
| vs Audacity | `/vs-audacity/` | SoftwareApp + Breadcrumb |
| vs GarageBand | `/vs-garageband/` | SoftwareApp + Breadcrumb |
| Alternatives | `/alternatives/` | SoftwareApp + Breadcrumb |
| Privacy | `/privacy/` | — |
| Disclaimer | `/disclaimer/` | — |
| 404 | `/404.html` | — |

---

## 1000+ Keywords — 5 Layers

| Layer | Detail |
|---|---|
| `<meta name="keywords">` | 100+ keyword phrases covering every audio recording search angle |
| `<title>` + `<meta description>` | Unique per page, keyword-rich, under character limits |
| JSON-LD schema | SoftwareApp + BreadcrumbList on all · FAQPage on /faq/ and /pricing/ · Review on /review/ · HowTo on /how-it-works/ and /record-streaming-audio/ · ItemList on /features/ · Article on all guide pages |
| Keyword-rich prose | Every page built around target keywords naturally embedded in content |
| SEO metadata | robots, canonical, og:, twitter:, rss alternate link on every page |

---

## SEO Files

| File | Purpose |
|---|---|
| `sitemap.xml` | 20 URLs with `lastmod`, priority and changefreq |
| `robots.txt` | Allows all crawlers, points to sitemap |
| `llms.txt` | 99-line product summary for AI crawlers (Perplexity, ChatGPT, etc.) |
| `feed.xml` | RSS feed with 5 blog articles |
| `assets/favicon.svg` | Purple microphone favicon |
| `.nojekyll` | Prevents GitHub Pages from running Jekyll |

**Submit sitemap after deploying:**
```
https://brightlane.github.io/audiorecorder/sitemap.xml
```
→ Google Search Console → Add property → Submit sitemap
→ Bing Webmaster Tools → Import from Google

---

## Product Facts

| Fact | Value |
|---|---|
| Product | Wondershare Streaming Audio Recorder |
| Version | 2.1.0 |
| Publisher | Wondershare Software Ltd (est. 2003, publicly listed) |
| Platform | Windows only (7, 8, 10, 11 — 32 and 64-bit) |
| Mac | Not available |
| Recording | System audio via virtual driver + microphone |
| Formats | MP3, WAV, FLAC, AAC, M4A, OGG, WMA, AIFF, AC3, APE |
| Key features | Scheduled recording, auto track split, ID3 tag editor, built-in editor, noise reduction, format converter |
| Pricing | Free trial · ~$29.95/yr Annual · Perpetual one-time |
| Review score | 8.8/10 |

---

## Design System

| Variable | Value | Usage |
|---|---|---|
| `--acc` | `#7c3aed` | Primary purple — CTAs, headings |
| `--acc2` | `#ec4899` | Pink — gradient accents |
| `--acc3` | `#06b6d4` | Cyan — code chips, info |
| `--gold` | `#f59e0b` | Gold — stars, warnings |
| `--green` | `#10b981` | Green — checkmarks |
| `--bg` | `#04050d` | Deep dark background |
| `--txt` | `#f0f0ff` | Primary text |
| `--muted` | `#7878a8` | Body / secondary text |

Fonts: **Fraunces** (headings, serif) + **Outfit** (body, sans) + **JetBrains Mono** (code).

---

## File Structure After Build

```
audiorecorder-site/
├── .nojekyll
├── index.html
├── 404.html
├── sitemap.xml
├── robots.txt
├── llms.txt
├── feed.xml
├── assets/
│   └── favicon.svg
├── features/index.html
├── how-it-works/index.html
├── use-cases/index.html
├── formats/index.html
├── pricing/index.html
├── review/index.html
├── faq/index.html
├── download/index.html
├── blog/index.html
├── record-streaming-audio/index.html
├── record-zoom-audio/index.html
├── record-spotify/index.html
├── podcast-recorder/index.html
├── voice-recorder/index.html
├── vs-audacity/index.html
├── vs-garageband/index.html
├── alternatives/index.html
├── privacy/index.html
└── disclaimer/index.html
```

---

## Tech Stack

| Layer | Choice |
|---|---|
| Generator | Python 3 stdlib only — zero dependencies |
| HTML/CSS/JS | Vanilla — no frameworks |
| Fonts | Google Fonts CDN (Fraunces + Outfit + JetBrains Mono) |
| Hosting | GitHub Pages — free, HTTPS, global CDN |
| CI/CD | GitHub Actions — auto-deploy on `git push` to `main` |

---

## License

Independent affiliate guide. Wondershare Streaming Audio Recorder is a product of Wondershare Software Ltd.
This site is not affiliated with or endorsed by Wondershare.

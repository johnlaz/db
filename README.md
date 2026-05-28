# DraftBound — Career Launchpad for Youth Athletes

> **Turn sideline moments into a recruiter-ready profile in under 5 minutes.**

[![Live App](https://img.shields.io/badge/Launch%20App-DraftBound-1A2850?style=for-the-badge&logo=googlechrome&logoColor=white)](https://johnlaz.github.io/db/app)
[![PWA Ready](https://img.shields.io/badge/PWA-Installable-378ADD?style=for-the-badge)](https://johnlaz.github.io/db/app)
[![Free to Use](https://img.shields.io/badge/Price-Free%20to%20Start-27AE60?style=for-the-badge)](https://johnlaz.github.io/db/app)

---

## What is DraftBound?

DraftBound is a mobile-first, AI-powered athletic recruiting tool built for parents. At a game, at a tournament, or on the sideline with no signal — parents open DraftBound, drop in photos, videos, or a photo of the scoresheet, and the app builds a professional recruiting profile automatically.

No design skills. No subscription. No complicated setup.

Coaches receive a polished, always-live profile link — with stats, highlights, a narrative bio, and a clean layout — that looks like it was built by a professional recruiting agency.

---

## Features

### 🎯 5-Minute Ingest Flow
Drop media at the game. The app queues everything offline first so bad stadium WiFi never loses a moment. Run the AI pipeline when you're ready.

### 🤖 AI Producer Pipeline
Powered by Google Gemini. The AI tags media automatically, parses stats directly from scoresheet photos (no manual entry), and generates recruiter-ready captions and bios.

### ⚡ Persona Engine
Four narrative styles — The Grinder, The Playmaker, The Leader, The Specialist — or build a fully custom persona in 4 questions using the AI Wizard. Every profile tells a story coaches remember.

### 📊 Sport-Aware Stats
18 sports with position-specific stat templates built in. Baseball, soccer, basketball, football, lacrosse, volleyball, swimming, track, softball, wrestling, tennis, cross country, hockey, golf, gymnastics, fishing, cheerleading, water polo. Add custom stats for anything else.

### 👁️ Admin Toggle System
Parents control exactly what recruiters see. Toggle any stat, photo, or video visible or hidden with one tap. The recruiter view updates instantly.

### 🌐 Live Recruiter Link
One shareable URL. Always live. Every update you make is reflected immediately — no re-sending links.

### 📱 PNG Share Card
Export a 1080×1080 branded card with the athlete's name, stats, persona, and recruiter URL. Ready to post to Instagram or text directly to a coach.

### 🖨️ PDF Print
A print-optimized recruiter view with branded header and footer — ready for a coach's binder or a college fair.

### 🌍 Deploy a Recruiting Website
Export a complete recruiting website in 3 visual styles (Spotlight, Stat Wall, Narrative). Upload to GitHub Pages for free. Your athlete gets a real URL for their resume.

### 📴 Offline First
Built with a service worker and IndexedDB. The full app works without an internet connection — critical for sideline use at fields and gyms with no signal.

### 🔒 Private by Default
All data stays on the parent's device. No cloud accounts. No data sold. The Gemini API key is stored locally only. Export a backup file anytime.

---

## Supported Sports

| Field | Court | Water | Track | Other |
|---|---|---|---|---|
| Soccer | Basketball | Swimming | Cross Country | Fishing |
| Lacrosse | Volleyball | Water Polo | Track & Field | Cheerleading |
| Baseball | — | — | — | Golf |
| Softball | — | — | — | Gymnastics |
| Football | — | — | — | Wrestling |
| Hockey | — | — | — | Tennis |

---

## Tech Stack

| Layer | Technology |
|---|---|
| App shell | Single-file HTML PWA — no build tools, no framework |
| Storage | IndexedDB (local-first) |
| AI | Google Gemini 1.5 Flash (vision + text) |
| Fonts | Barlow Condensed + DM Sans |
| Offline | Service Worker (cache-first) |
| Install | Web App Manifest (iOS + Android) |
| Export | Canvas API (PNG), Print API (PDF), Blob (HTML) |

---

## Repo Structure

```
/
  index.html              ← Marketing landing page
  README.md
  assets/
    hero.jpg              ← Landing page hero photo (900×1200px)
    sport-1.jpg           ← Sports strip photos (600×800px each)
    sport-2.jpg
    sport-3.jpg
    sport-4.jpg
    sport-5.jpg
    feature.jpg           ← Feature section background (800×600px)

  app/
    index.html            ← DraftBound PWA application
    manifest.json         ← PWA install manifest
    sw.js                 ← Service worker (offline support)
    assets/
      icon-192.png        ← App icon (Android home screen)
      icon-512.png        ← App icon (splash screen)
      icon-maskable.png   ← App icon (adaptive, Android)
      apple-touch-icon.png ← App icon (iOS home screen)
```

---

## Getting Started

### Use the app
Open [https://johnlaz.github.io/db/app](https://johnlaz.github.io/db/app) on your phone and tap **Add to Home Screen** to install as a PWA.

### Set up AI features
1. Get a free Gemini API key at [ai.google.dev](https://ai.google.dev)
2. Open DraftBound → Settings → Gemini API key → paste your key
3. Your key is stored only on your device — never sent to any server other than Google's API

### Add your athlete
1. Open Settings → Athletes → Add new athlete
2. Set their name, sport, position, graduation year, and GPA
3. Tap Persona → choose a style or build a custom one with the AI Wizard
4. Head to Ingest and start dropping media

---

## Deploying an Athlete's Recruiting Website

1. In DraftBound, go to **Share → Choose style & export**
2. Pick Spotlight, Stat Wall, or Narrative
3. Tap **Export index.html** — file saves to your downloads
4. Create a free GitHub account and a new repository
5. Upload `index.html` to the repo root
6. Go to **Settings → Pages** → set source to main branch
7. Your athlete's recruiting page is live at `https://yourusername.github.io/reponame`

---

## Roadmap

- [ ] Gemini Vision stat parsing (live with API key)
- [ ] Video highlight reel trimming
- [ ] Multi-season stat history charts
- [ ] Coach contact / express interest flow
- [ ] Team roster mode (coaches building profiles for full rosters)
- [ ] QR code for recruiter view URL

---

## License

Built by [LAZLAB Creations](https://johnlaz.github.io). All rights reserved.

DraftBound is free to use. The Gemini API is provided by Google and subject to [Google's terms of service](https://ai.google.dev/terms). All athlete data is stored locally on the user's device.

---

*DraftBound — Because every athlete deserves a shot.*

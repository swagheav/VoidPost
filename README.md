<h3 align="center">VOID//POST — Facebook Page Publishing Console</h3>

<p align="center">
  Single-file Flask web GUI for publishing to Facebook Pages via the official Graph API.<br>
  Fast · Local · Official API only
</p>

<p align="center">
  <img src="https://img.shields.io/badge/VOID-POST-red?style=for-the-badge&logo=facebook&logoColor=white" alt="VoidPost"/>
  <img src="https://img.shields.io/badge/Python-3.x-blue?style=for-the-badge&logo=python" alt="Python"/>
  <img src="https://img.shields.io/badge/Flask-Web%20UI-green?style=for-the-badge&logo=flask" alt="Flask"/>
  <img src="https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge" alt="License"/>
  <img src="https://img.shields.io/badge/Made%20in-2026-purple?style=for-the-badge" alt="2026"/>
</p>

---

## Overview

**VOID//POST** is a self-hosted web GUI for posting to **Facebook Pages** you manage, through Facebook's **official Graph API**. No scraping, no unofficial endpoints — it uses a Page access token you provide and talks only to `graph.facebook.com`.

It supports **text posts**, **photo posts**, and **multi-post batch publishing** in a single session, wrapped in the same terminal-styled VOID UI as the rest of the suite.

---

## Features

- Connect via Page ID + access token (validated live against the Graph API)
- Publish text-only posts to a Page feed
- Publish photo posts with caption
- Compose up to **10 posts per batch** and publish sequentially
- Long-lived token exchange helper (App ID + App Secret + short-lived token)
- Credentials saved locally to `~/.fb_poster_gui_config.json`
- Activity log with timestamps and per-post status
- Confirmation modal before publishing
- Terminal-styled UI with scanlines, grain, and mono fonts

---

## Requirements

| Component | Minimum |
|-----------|---------|
| OS | Windows / Linux / macOS |
| Python | 3.7+ |
| Browser | Any modern browser |
| Facebook | A Page you manage + a Page access token |
| Internet | Required |

---

## Installation

```bash
# Clone the repository
git clone https://github.com/swagheav/VOID-POST.git
cd VOID-POST

# Install dependencies
pip install flask requests

# Run
python voidpost.py
```

Then open **http://127.0.0.1:5000** in your browser.

---

## Usage

### 1. Get a Page access token

You need a **Page access token** with these permissions:
- `pages_manage_posts`
- `pages_read_engagement`

**Fast path (dev testing):**
1. Go to [developers.facebook.com/tools/explorer](https://developers.facebook.com/tools/explorer)
2. Select your app
3. Click **Get Page Access Token** → grant permissions → select your Page
4. Copy the token and paste it into VOID//POST

**Long-lived path (production):**
1. Use the **[ + ] Get a long-lived token** panel in the app
2. Fill App ID, App Secret, and short-lived user token
3. Click **Exchange** — the app swaps it for a 60-day token and fills it in

### 2. Connect

1. Go to the **Connect** tab
2. Paste your **Page ID** and **token**
3. Click **Test connection** — you should see your Page name appear
4. Click **Save credentials** to persist locally

### 3. Compose and publish

1. Switch to **Compose**
2. Type your post (add a photo if you want)
3. Click **+** to add more posts (up to 10)
4. Click **Publish** → confirm the modal → done

---

## Project Structure

```
VOID-POST/
├── voidpost.py        # Flask app + frontend
├── requirements.txt   # flask, requests
├── README.md
└── LICENSE
```

---

## Technical Details

| Property | Details |
|----------|---------|
| Language | Python 3.x |
| Framework | Flask |
| API | Facebook Graph API v21.0 |
| Endpoints | `/feed`, `/photos`, `/oauth/access_token` |
| Frontend | Single-file HTML/CSS/JS |
| Storage | Local JSON config only |
| Batch size | 10 posts max |

---

## Notes

- This tool is for **Pages you own or manage**. It will not work on personal profiles or Pages you don't have permission to post to.
- All requests go to Facebook's official API — no scraping, no unofficial endpoints.
- Keep your token private. Don't commit `~/.fb_poster_gui_config.json` to git.

---

## Developer

| Contact | Link |
|---------|------|
| Telegram | [@SWGHEV](https://t.me/SWGHEV) |
| GitHub | [@swagheav](https://github.com/swagheav) |

---

<p align="center">© 2026 VOID//POST • All Rights Reserved</p>

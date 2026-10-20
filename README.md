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

<p align="center">
  <b>Developer:</b> #SWAG – Heaven Swag ·
  <a href="https://t.me/he6ca">DM</a> ·
  <a href="https://t.me/SWGHEV">Channel</a>
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
git clone https://github.com/swagheav/VoidPost.git
cd VoidPost

# Install dependencies
pip install flask requests

# Run
python voidpost.py

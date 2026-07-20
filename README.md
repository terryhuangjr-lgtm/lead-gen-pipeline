<h1 align="center">📊 Lead Gen Pipeline</h1>
<p align="center">
  <b>Automated Local Business Discovery & Outreach</b>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.12-3776AB?logo=python" alt="Python"/>
  <img src="https://img.shields.io/badge/Google_Maps_API-4285F4?logo=googlemaps" alt="Google Maps"/>
  <img src="https://img.shields.io/badge/Gmail_API-EA4335?logo=gmail" alt="Gmail"/>
  <img src="https://img.shields.io/badge/Supabase-FF4438?logo=supabase" alt="Supabase"/>
  <img src="https://img.shields.io/badge/Claude_AI-FF6600?logo=anthropic" alt="Claude"/>
  <img src="https://img.shields.io/badge/Status-Production_Deployed-22c55e" alt="Status"/>
</p>

---

## 📋 The Problem

Finding qualified local business leads for an AI agency is manual and tedious. Searching Google Maps, checking websites, writing personalized outreach — it takes hours per lead and scales poorly.

## 💡 The Solution

An automated pipeline that discovers local businesses fitting your ideal customer profile, enriches them with contact info and website data, scores their fit, and generates personalized Gmail outreach drafts — all on a scheduled cadence.

---

## ✨ How It Works

```
┌────────────────┐    ┌────────────────┐    ┌────────────────┐
│  Google Maps   │    │  Website       │    │  AI Scoring    │
│  Places API    │───▶│  Scraper       │───▶│  + Enrichment  │
└────────────────┘    └────────────────┘    └────────┬───────┘
                                                     │
                                            ┌────────▼───────┐
                                            │  Gmail Draft   │
                                            │  Generator     │
                                            └────────────────┘
```

### Step-by-step

1. **Discovery** — Search Google Maps Places API for businesses in target categories (e.g. "NYC property management", "NJ physical therapy")
2. **Enrichment** — Visit each business's website to extract services, size, tech stack, and contact info
3. **Scoring** — AI evaluates fit based on your ideal customer profile (size, industry, tech readiness)
4. **Outreach Drafting** — For high-scoring leads, generate a personalized Gmail draft with context about their business
5. **Scheduling** — Runs on a configurable cron schedule with daily digest of new leads found

## 🛠 Tech Stack

- **Language:** Python
- **Discovery:** Google Maps Places API
- **Enrichment:** Web scraping + Claude AI
- **Database:** Supabase (PostgreSQL)
- **Outreach:** Gmail API (via Google Workspace)
- **Scoring:** Claude AI + custom heuristics
- **Scheduling:** Cron-based pipeline
- **Deployment:** Local system (Hermes Agent)

## 🚀 Status

**🟢 Production deployed** — actively discovering and qualifying leads for Level Up Digital's AI agency services.

---

## 🏁 Getting Started

```bash
git clone https://github.com/terryhuangjr-lgtm/lead-gen-pipeline.git
cd lead-gen-pipeline

python -m venv venv
source venv/bin/activate
pip install -r requirements.txt

cp .env.example .env
# Add: Google Maps API key, Gmail credentials, Claude API key

python pipeline.py
```

# Stock Market Dashboard

A real-time stock tracking platform with live price charts and AI-personalized daily email digests.

🔗 **Live:** https://stock-tacker-app.vercel.app

---

## Features

- Real-time stock charts via TradingView widgets
- Stock search powered by Finnhub API
- Personal watchlist management
- AI-personalized daily email digest based on watchlist
- Background job processing via Inngest
- Gemini AI for generating personalized market summaries
- Email delivery via Nodemailer

## Tech Stack

**Frontend:** Next.js 15, React 19, Tailwind CSS, Radix UI

**Backend:** Next.js Server Actions, Next.js API Routes

**Database:** MongoDB with Mongoose

**Auth:** Better Auth with MongoDB adapter

**Background Jobs:** Inngest (cron + serverless queues)

**External APIs:** Finnhub API, TradingView Widgets

**AI:** Gemini 2.5 Flash Lite

**Email:** Nodemailer (SMTP)

## How It Works

1. User signs up with email and investment preferences
2. Gemini AI generates a personalized welcome email via Inngest
3. User searches stocks via Finnhub and adds them to their watchlist
4. TradingView widgets display live price charts
5. Every day at 12PM, Inngest fetches watchlist news from Finnhub and sends a Gemini-summarized email digest

## Run Locally
```bash
git clone https://github.com/fayiskooni/YOUR_REPO_NAME
npm install

# Add environment variables
# MONGODB_URI, FINNHUB_API_KEY, GEMINI_API_KEY
# INNGEST_EVENT_KEY, INNGEST_SIGNING_KEY
# SMTP credentials for Nodemailer

npm run dev
```

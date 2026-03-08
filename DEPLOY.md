# Hotel Bot (Destin & Pensacola Beach) — Deployment Guide

## Trigger.dev Project
Project ID: `proj_lpvgerjdqfhvhgzyeiss`

## Environment Variables
Add these in Trigger.dev → Project Settings → Environment Variables:

| Variable | Value |
|---|---|
| `RAPIDAPI_KEY` | your RapidAPI key |
| `ANTHROPIC_API_KEY` | your Anthropic key |
| `EXPEDIA_AFFILIATE_ID` | `1100l395625` |
| `FACEBOOK_PAGE_ID` | `1058965420626510` |
| `FACEBOOK_PAGE_ACCESS_TOKEN` | your long-lived FB token |

## Deploy Command
Run from the `hotel_bot_triggerdev` folder:
```bash
npx trigger.dev@latest deploy
```

## Schedule
- **9am CT daily** → Destin, FL post
- **2pm CT daily** → Pensacola Beach, FL post

## Verify After Deploying
1. Go to your Trigger.dev project
2. Switch to Production environment
3. Click Tasks — should see `hotel-facebook-bot-morning` and `hotel-facebook-bot-afternoon`
4. Check Schedules tab — should show both scheduled times

## ⚠️ Important
This project ID (`proj_lpvgerjdqfhvhgzyeiss`) is for THIS bot only.
Always deploy from this folder — never from another bot's folder.

## Facebook Token Renewal
Long-lived tokens expire after ~60 days. Set a calendar reminder to refresh your
Facebook Page Access Token at: https://developers.facebook.com/tools/explorer/

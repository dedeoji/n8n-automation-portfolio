# Social Media Content Scheduler

**Demo video and case study:** [samueloji.netlify.app](https://samueloji.netlify.app)

## The problem

Coaches know consistency matters, but between client sessions, course updates and DMs, posting is the first thing that slips. Posting the same content to three platforms by hand takes hours each week.

## What it does

- Checks a Google Sheet content calendar every 15 minutes
- Publishes approved posts that are due to LinkedIn, a Facebook Page and Instagram (text and images, with a separate caption per platform if wanted)
- Checks every post before it goes out, and writes every result back to the sheet with a link to the live post
- Marks any failure (a missing image, a caption that's too long, an expired login) in the sheet and sends a Telegram alert with the exact reason
- Tracks each platform separately, so nothing is ever posted twice

**Tested result:** one row went out on all three platforms at its scheduled time, and a post with a missing image was caught and flagged within the same minute.

## Workflows in this folder

| File | What it does |
|------|--------------|
| `scheduler-linkedin-facebook-instagram.json` | The main scheduler: LinkedIn, Facebook Page and Instagram |
| `scheduler-linkedin-x-instagram.json` | A variant that posts to X instead of Facebook |
| `error-notifier.json` | Error workflow: sends a Telegram alert if a scheduler run fails |

Instagram publishing uses the Graph API's two-step flow: create a media container, wait until its status is `FINISHED`, then publish.

## Setup

Set your sheet ID, Facebook Page ID, Instagram account ID and Telegram chat ID in the **Config** node (all shown as `YOUR_...` placeholders).

## Stack

n8n · Google Sheets · LinkedIn API · Meta Graph API (Facebook & Instagram) · X API · Telegram · JavaScript

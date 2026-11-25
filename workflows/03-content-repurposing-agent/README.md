# AI Content Repurposing Agent

**Demo video and case study:** [samueloji.netlify.app](https://samueloji.netlify.app)

## The problem

Coaches already create their best content every week, in masterclasses, live sessions and webinars. Turning that into daily posts means hours of rewriting, and posts written by someone else (or by AI on its own) sound generic, not like the coach. So the masterclass is taught once and the ideas never reach the feed.

## What it does

- A simple form: paste a transcript, add a title, pick the first post date
- Reads the coach's profile (who she helps, her offers, words to avoid) and a set of her past posts from Google Sheets
- GPT-4o writes one post per idea from the masterclass, with a LinkedIn, Facebook and Instagram version of each, in her voice, using her stories, phrasing and formatting, never invented facts
- Adds each post to the content calendar as a draft, one per day at her usual posting time, marked **Not Approved**
- Nothing goes out until she approves it; approved posts are published by the [Social Media Content Scheduler](../05-social-media-scheduler)

**Tested result:** one form submission produced 7 days of posts for 3 platforms (21 captions) in under 30 seconds.

## Workflow

| File | Nodes |
|------|-------|
| `content-repurposing-agent.json` | Repurpose Form → Config → Read Coach Profile → Read Voice → Build Prompt (JavaScript) → Write Posts (OpenAI) → Prepare Rows (JavaScript) → Add to Calendar (Google Sheets) |

## Setup

Set your Google Sheet ID in the **Config** node (`YOUR_GOOGLE_SHEET_ID`). The sheet needs a coach profile tab, a past posts (voice) tab and a content calendar tab.

## Stack

n8n Forms · OpenAI (GPT-4o) · Google Sheets · JavaScript

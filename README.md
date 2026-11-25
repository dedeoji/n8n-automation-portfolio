# n8n Automation Portfolio

Automations that give online coaches and course creators their time back: answering students 24/7, replying to leads in seconds, and keeping content going out while they focus on clients.

Every project here is a real, tested build: the problem, what I built, and the n8n workflows behind it, ready to import.

**Demos and case studies:** [samueloji.netlify.app](https://samueloji.netlify.app) · **LinkedIn:** [Samuel Oji](https://www.linkedin.com/in/samuel-nkemakolam)

---

## Projects

| # | Project | What it does for the coach | Built with |
|---|---------|----------------------------|------------|
| 01 | [AI WhatsApp Lead Setter (UK GDPR)](workflows/01-whatsapp-lead-setter) | Replies to new WhatsApp leads in seconds, qualifies and scores them, books good fits into the diary, follows up once, and hands medical questions to the coach. UK GDPR built in. | n8n, OpenAI, WhatsApp Cloud API, Supabase (Postgres), Cal.com, Gmail, SQL, JavaScript |
| 02 | [AI Student Support Agent (RAG)](workflows/02-student-support-agent-rag) | Answers students 24/7 from the academy's own knowledge base, remembers the conversation, and hands refunds and personal issues to a human. | n8n, OpenAI, Supabase (pgvector), Postgres chat memory, Gmail |
| 03 | [AI Content Repurposing Agent](workflows/03-content-repurposing-agent) | Turns one masterclass transcript into a week of LinkedIn, Facebook and Instagram posts in the coach's own voice, waiting for approval. | n8n Forms, OpenAI (GPT-4o), Google Sheets |
| 04 | [Multi-Channel AI Support Agent](workflows/04-multichannel-support-agent) | One AI agent answering website chat, email and WhatsApp (including voice notes) from the same knowledge, with escalation to a human. | n8n, OpenAI, WhatsApp Cloud API, Gmail, Google Sheets |
| 05 | [Social Media Content Scheduler](workflows/05-social-media-scheduler) | Publishes approved posts from a Google Sheet to LinkedIn, Facebook and Instagram on schedule, logs every result and alerts on failures. | n8n, Google Sheets, LinkedIn API, Meta Graph API, Telegram |

The businesses in the demos (Second Wind Coaching, Kestrel Coach Academy, Tillstone) are fictional. The workflows, integrations and tests are real.

---

## How to import a workflow

1. In n8n, create a new workflow, then **⋯ → Import from File** and choose the `.json` file.
2. Open each node marked with a warning and connect your own credentials (OpenAI, Supabase, Gmail, WhatsApp and so on).
3. Replace the placeholders, such as `YOUR_GOOGLE_SHEET_ID`, `YOUR_WHATSAPP_PHONE_NUMBER_ID` and `you@example.com`, with your own values.
4. Each project's README lists any database tables or sheets it needs.

All credentials, account IDs, phone numbers and email addresses have been removed from these exports.

---

## About me

I'm Samuel Oji, an AI automation specialist. I build AI agents and automations for online coaches and course creators, mostly in n8n, with JavaScript, SQL and Postgres (Supabase), OpenAI, the WhatsApp Cloud API and Docker.

Want something like this for your business? [Book a free automation audit](https://samueloji.netlify.app).

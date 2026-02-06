# Daily Cybersecurity News Email Automation (n8n)

## Description
This n8n workflow automatically collects the latest **cybersecurity news and events** every day and sends them as a **well-formatted email summary**.

It pulls news from trusted cybersecurity websites and Google Events, summarizes the content using **Google Gemini (AI)**, and emails the digest using **Gmail**.

---

## What This Workflow Does (Simple Explanation)

Every day, the workflow:
1. Fetches cybersecurity news articles
2. Fetches cybersecurity-related events
3. Combines all data into one list
4. Uses AI to summarize each article
5. Sends the summary as an email

---

## Trigger

- **Schedule Trigger**
  - Runs **once per day**
  - Timezone: `Asia/Kolkata`
  - Time can be changed easily

---

## News Sources Used

### RSS Feeds
- **The Hacker News**
- **BleepingComputer**

### API Source
- **SERP API (Google Events)**
  - Example query: *Cyber Events in India*

---

## Workflow Steps (Beginner Friendly)

1. **Schedule Trigger**
   - Starts the workflow automatically every day.

2. **RSS Feed Nodes**
   - Fetch cybersecurity news articles from websites.

3. **HTTP Request Node**
   - Fetches cybersecurity events using SERP API.

4. **Merge Node**
   - Combines RSS articles and API event data.

5. **Aggregate Node**
   - Groups all news into a single dataset.

6. **AI Summarization (Gemini)**
   - Creates:
     - Headlines in ALL CAPS
     - 3–4 sentence summaries
     - Article links
   - Formats everything like a newsletter email.

7. **Gmail Node**
   - Sends the summarized news to email recipients.

---



## Email Output

You will receive:
- One daily email
- Cybersecurity headlines in ALL CAPS
- Short summaries explaining why the news matters
- Links to original articles

---

## Requirements

- n8n (local or cloud)
- SERP API key
- Google Gemini (PaLM) API key
- Gmail account
- Internet connection

---

## File Information

- Workflow file: `NEWS_LETTER.json`
- Platform: **n8n**
- AI Model: **Google Gemini**
- Email Service: **Gmail**

---

## Notes

- You can change the email time in the Schedule Trigger.
- API limits may affect how much data is fetched.
- RSS feeds depend on external websites.

---

## Author
Built using **n8n automation**, **Gemini AI**, and **public cybersecurity news sources**.

# Daily Cybersecurity News Digest Automation

## Overview
This n8n workflow automatically collects the latest **cybersecurity news and events** from multiple sources, formats them using an LLM (Gemini), and sends a **daily email digest**.

It eliminates the need to manually browse multiple websites and provides a concise, readable cybersecurity summary once per day.

---

## Workflow Purpose
- Collect cybersecurity news from multiple sources
- Merge and organize all events
- Use an LLM to generate structured summaries
- Deliver a single daily email digest via Gmail

---

## Trigger
- **Cron Trigger**
  - Runs **once per day**

---

## Data Sources
- **RSS Feeds**
  - Multiple cybersecurity news websites
- **HTTP Request**
  - Uses **SARP API**
  - `get_event` search engine for cybersecurity-related events

---

## Workflow Steps

1. **Trigger Node**
   - Initiates the workflow once per day.

2. **RSS Feed Nodes**
   - Fetch cybersecurity news articles from different websites.

3. **HTTP Request Node**
   - Fetches cybersecurity events using the **SARP `get_event` API**.

4. **Merge Node**
   - Combines all RSS feed data and API responses into a single dataset.

5. **Aggregate Node**
   - Separates and organizes each cybersecurity event/article.

6. **LLM (Gemini) Node**
   - Formats each article into a structured email-ready format.
   - Generates headlines, summaries, and preserves article links.

7. **Gmail Node**
   - Sends the final formatted cybersecurity news digest via email.

---

## LLM Prompt (Gemini)

The following prompt is used **without modification** to format the cybersecurity news:

You are an News Summerizer Assistant
Analyze the news articles and create an email summary.

** Dont change the default language **
**For each article**
 - 1.Create a headline in ALL CAPS
 - 2.Write a 3-4 sentence summary
 - 3.Include the article link

Format as
Subject: Today's Cybersecurity News

Hi there,

Here's your Cyber-Security news Summary.

serial number. HEADLINE IN CAPS

Summary of what happened and why it matters...

Read more: [Link]

Best regards,
AI News Bot.


---

## Inputs & Requirements

- **API Keys**
  - SARP API key
  - Gemini API key

- **Email Setup**
  - Gmail account connected to n8n
  - Required Gmail permissions enabled

- **RSS Feed URLs**
  - Cybersecurity-related news sources

---

## Output
- A **daily email** containing:
  - ALL CAPS headlines
  - 3–4 sentence summaries per article
  - Direct links to original sources

---

## Use Cases
- Daily cybersecurity awareness
- Security research and learning
- Personal or team news digest
- SOC / security team updates

---

## Notes & Limitations
- Output quality depends on article content and LLM response.
- API rate limits may affect the number of fetched articles.
- RSS feed availability depends on external sources.

---

## File
- Workflow export: `NEWS_LETTER.json`

---

## Author
Built using **n8n**, **Gemini LLM**, and **SARP APIs** for automated cybersecurity news monitoring.




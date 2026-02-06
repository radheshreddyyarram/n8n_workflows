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

## Setup Instructions (Step by Step)

### Step 1: Install or Access n8n
- Use **n8n Cloud** OR
- Run n8n locally using Docker or Node.js

👉 Make sure you can access the **n8n Editor UI**.

---

### Step 2: Import the Workflow
1. Open n8n Editor
2. Click **Import Workflow**
3. Upload the file:

---

### Step 3: Configure RSS Feeds (Optional)
- Open the RSS nodes:
- `TheHackerNews`
- `Bleepingcomputer`
- You can:
- Keep existing URLs, or
- Replace them with other cybersecurity RSS feeds

---

### Step 4: Setup SERP API
1. Create an account at **SERP API**
2. Copy your **API key**
3. Open the **HTTP Request** node
4. Replace the existing `api_key` value with your own key

---

### Step 5: Setup Google Gemini (AI)
1. Create a **Google Gemini (PaLM) API key**
2. In n8n:
- Go to **Credentials**
- Add **Google Gemini (PaLM) API**
3. Connect the credential to the **Gemini node**

---

### Step 6: Setup Gmail
1. Go to **Credentials** in n8n
2. Add **Gmail OAuth2**
3. Sign in with your Gmail account
4. Open the **Gmail node**
5. Update:
- `Send To` email address
- `BCC` list (optional)

---

### Step 7: Test the Workflow
1. Click **Execute Workflow**
2. Check if:
- News is fetched
- Email is received successfully

---

### Step 8: Activate the Workflow
- Turn the workflow **ON**
- It will now run automatically every day

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

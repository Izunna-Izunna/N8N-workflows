# 🤖 Reply X – n8n Twitter Scraper & Character Responder

This repository contains a powerful [n8n](https://n8n.io/) workflow called **Reply X** that:

- Fetches relevant tweets using a custom Twitter API
- Parses and enriches the tweets with metadata
- Saves tweet data to Google Sheets
- Combines tweet content with character profiles
- Generates custom prompts to help AI personas craft tailored replies

> Designed for creators, indie hackers, and automation lovers.

---

## 🚀 Features

- 🔍 **Advanced Twitter Search**  
  Uses `twitterapi.io` to fetch top tweets related to:
  - `#buildinpublic`, `#indiehacker`, `#founder`, `#nocode`, `#saas`, and more
  - Tweets containing phrases like “need a website”, “build an MVP”, “automation help”

- 📑 **Custom Code Node**  
  Processes tweets to:
  - Format metadata
  - Add status flags (`waiting`)
  - Prepare for sheet integration

- 📊 **Google Sheets Integration**  
  Auto-appends tweet info like tweet ID, content, likes, views, replies, etc.

- 🧠 **Character AI Prompt Builder**  
  Merges tweet data with character records to generate rich, story-based reply prompts

- 🕓 **Scheduled Automation**  
  Run the bot automatically at intervals or trigger it manually

---

## 🧰 Tech Stack

| Component       | Description                                     |
|----------------|-------------------------------------------------|
| n8n             | Workflow automation tool                        |
| HTTP Request    | Fetches tweets from custom API (`twitterapi.io`) |
| Code Node       | JavaScript logic to parse and transform tweets |
| Google Sheets   | Stores tweets and character profiles            |
| Merge Node      | Joins tweet and character data                  |
| Final Code Node | Generates structured prompt for AI personas    |

---

## 📁 Structure

N8N-workflows/
├── workflows/
│ └── reply-x.json # The core n8n workflow file
├── .gitignore
├── README.md
└── LICENSE (optional)

---

## 🛠 Setup Instructions

### 1. Clone this Repo

```bash
git clone https://github.com/Izunna-Izunna/N8N-workflows.git
cd N8N-workflows
2. Import into n8n
Open your n8n instance

Go to "Workflows" → "Import from File"

Upload workflows/reply-x.json

3. Set Credentials
Twitter API via httpHeaderAuth

Google Sheets OAuth2 for reading/writing character & tweet data

✨ Use Case Example
Let’s say you roleplay 3 AI personas on Twitter:

A witty indie founder 🧠

A helpful automation bot 🤖

A chill SaaS bro 😎

This bot will:

Fetch tweets where people ask for help or mention #buildinpublic

Store those tweets in a sheet

Combine each with a character persona

Generate a tweet reply prompt in their unique voice


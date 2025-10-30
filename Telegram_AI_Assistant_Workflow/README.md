# 🤖 Telegram AI Assistant Workflow

The **Telegram AI Assistant Workflow** is an end-to-end automation built with **n8n** that turns your Telegram bot into a smart personal assistant powered by **OpenAI**.  
It can chat, transcribe voice messages, summarize emails, and manage your Google Calendar — all through a single Telegram chat.

---

## ✨ Features

- 💬 **Chat via Telegram** — seamless two-way communication with an AI.
- 🧠 **AI-Powered Responses** — uses OpenAI’s GPT-4o model for intelligent, context-aware replies.
- 🗣️ **Voice-to-Text Support** — transcribes Telegram voice messages using OpenAI Whisper.
- 📅 **Google Calendar Integration**
  - Create, view, and manage events using natural language.
- 📧 **Gmail Integration**
  - Summarize recent emails or send new ones using simple commands.
- 🧩 **Session Memory**
  - Maintains short-term conversational memory using **LangChain’s Memory Buffer Window**.
- ⚙️ **Multi-Tool Support**
  - Dynamically switches between Gmail, Calendar, and AI functions based on context.

---

## 🧭 Workflow Overview

1. **Telegram Trigger**  
   Starts the workflow when a Telegram message or voice note is received.

2. **Switch Node**  
   Detects message type (`text` or `voice`).

3. **Voice Handling**  
   - Downloads voice message file from Telegram.  
   - Transcribes audio using OpenAI Whisper.

4. **AI Agent**  
   - Processes the text or transcribed input using GPT-4o.  
   - Utilizes connected tools (Gmail, Calendar) when needed.

5. **Response Delivery**  
   Sends the AI-generated response back to the user on Telegram.

---


## 🧩 Tech Stack

| Component | Purpose |
|------------|----------|
| **n8n** | Automation framework |
| **Telegram Bot API** | User chat interface |
| **OpenAI (GPT-4o & Whisper)** | AI reasoning + transcription |
| **LangChain** | Agent + memory orchestration |
| **Gmail API** | Email handling |
| **Google Calendar API** | Scheduling |
| **ngrok** | Local webhook tunneling |

---

## ⚙️ Setup Instructions

### 1. Prerequisites

- [n8n](https://n8n.io) instance (local or cloud)
- Telegram bot (via [@BotFather](https://t.me/BotFather))
- OpenAI API key
- Google credentials (OAuth for Gmail and Calendar)

---

### 2. Import the Workflow

1. Open your **n8n editor**.  
2. Click **Import Workflow**.  
3. Paste the provided JSON or upload the file.  
4. Connect credentials for:
   - **Telegram API**
   - **OpenAI API**
   - **Gmail OAuth2**
   - **Google Calendar OAuth2**

---

### 3. Start the Telegram Bot

Run your local tunnel (e.g., ngrok):

```bash
ngrok http 5678
```
---

### 4. Run the Workflow

Once everything is configured and your ngrok tunnel is active, simply **activate the workflow** inside n8n.  
Now, send a message or a voice note to your connected Telegram bot — the assistant will automatically process it and respond intelligently.

If you send:
- Text → It’ll reply using GPT-4o with natural, context-aware language.
- Voice → It’ll transcribe it using Whisper before generating a reply.

The assistant can also interpret natural commands like:
- “What emails did I get today?”
- “Add a meeting tomorrow at 3 PM.”
- “Send an email to Sarah saying I’m on my way.”

---

## 🧱 Future Improvements

- 🧩 **Add persistent long-term memory** beyond session windows  
- 📂 **Support for document uploads** and file-based Q&A  
- 👥 **Multi-user support** for group Telegram bots  
- 🔔 **Notifications or summaries** for unread emails or upcoming events  
- 🌐 **Integrations with other platforms** like Slack, Notion, or Drive

---




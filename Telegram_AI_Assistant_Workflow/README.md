# 🤖 Telegram AI Assistant Workflow

The **Telegram AI Assistant Workflow** is an end-to-end automation built with **n8n** that turns your Telegram bot into a smart personal assistant powered by **OpenAI**.  
It can chat, transcribe voice messages, summarize emails, and manage your Google Calendar — all through a single Telegram chat.

---

## ✨ Features

### 💬 Smart Chat
- Responds to text messages using OpenAI’s `gpt-4o` model.  
- Keeps context between chats using **Window Buffer Memory**.

### 🎙️ Voice Message Support
- Accepts Telegram voice notes.
- Automatically transcribes them using **OpenAI Whisper**.
- Replies intelligently just like with text input.

### 📧 Gmail Integration
- **Summarize** recent emails (`Gmail_Summary`).
- **Send** new emails via Gmail (`Gmail_Send`), signed as *Arnie*.

### 📅 Google Calendar Integration
- **Create** calendar events with natural commands.  
- **Retrieve** your upcoming appointments.

### 🧠 Context Awareness
- Each Telegram chat has its own persistent memory session.
- Enables multi-turn, context-aware conversations.

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

## ⚙️ Workflow Overview

```text
Telegram Trigger → Switch
 ├── Text → Edit Fields → AI Agent → Telegram Reply
 └── Voice → Download File → Transcribe → AI Agent → Telegram Reply

AI Agent ↔ Gmail / Calendar / Memory


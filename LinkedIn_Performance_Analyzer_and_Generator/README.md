# LinkedIn Performance Analyzer & Content Generator

Automated workflow that analyzes LinkedIn content performance, extracts insights from engagement data, and generates new posts with AI-created visuals.

---

## 🚀 What It Does

- Analyzes LinkedIn posts from profiles, companies, or hashtags  
- Extracts sentiment, engagement patterns, and insights from comments  
- Generates new LinkedIn posts based on what performs well  
- Creates AI-powered visuals matching your content  

---

## ✨ Features

- Automated data collection from LinkedIn  
- Sentiment analysis and pattern recognition  
- AI-powered content generation (text + images)  
- Professional image creation  
- Duplicate prevention  
- Organized output stored in Airtable tables  

---

## 🧰 Tech Stack

- **n8n** – Workflow automation  
- **Airtable** – Data management  
- **Apify** – LinkedIn scraping  
- **Google Gemini** – AI analysis & content generation  
- **Freepik API** – Image generation  

---

## 🛠️ Installation

### 1. Prerequisites

Create accounts and obtain API keys for:

- n8n (self-hosted or cloud)  
- Airtable API token  
- Apify API token  
- Google Gemini API key  
- Freepik API key  

---

### 2. Import Workflow

1. Clone this repository  
2. Import `linkedin-performance-analyzer-workflow.json` into **n8n**  
3. Configure API credentials inside n8n  

---

### 3. Setup Airtable

Create a base with **three tables**:

---

### **Dashboard Table**

| Field | Type |
|-------|------|
| URL/Hashtag/Company | Single line text |
| Type | Single select (Profile, Company, Hashtag) |
| numPosts | Number |
| Analyze Post | Button |

---

### **Analyzed Data Table**

| Field | Type |
|-------|------|
| Company/Hashtag/Profile name | Single line text |
| Linkedin Post Text | Long text |
| Linkedin Post Url | URL |
| Overall Sentiment | Single select (1–5) |
| Tool Helpfulness | Single select (1–5) |
| Common Questions | Long text |
| Key Insights | Long text |
| Likes / Shares / Comments | Number |
| Type | Single select |

---

### **Generated Assets Table**

| Field | Type |
|-------|------|
| Company/Hashtag/Profile name | Single line text |
| Generated Post Text | Long text |
| Generated Image | Attachment |
| Type | Single select |
| Reference Image | Attachment |

---

## 🔧 4. Update Configuration

Inside n8n, modify the following:

- **Airtable** → Base ID + Table IDs  
- **Apify HTTP Request nodes** → API token  
- **Freepik API** → Header authentication  

---

## 📘 Usage

### 📝 Analyze Posts

1. Open **Dashboard** table in Airtable  
2. Add a new record with:
   - Profile URL / Company name / Hashtag  
   - Type  
   - Number of posts to analyze  
3. Click **Analyze Post**  
4. View processed results in **Analyzed Data** table  

---

### ✍️ Generate Content

- In **Analyzed Data** table, check the **Generate Script** field  
- Generated post text will appear in **Generated Assets** table  

---

### 🖼️ Create Visuals

1. In **Generated Assets**, upload a **Reference Image** (optional)  
2. Check the **Generate Image** box  
3. AI-generated image will be added to the same record  

---

## 🧱 Workflow Architecture



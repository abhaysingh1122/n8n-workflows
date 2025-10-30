# 🌸 Nanobana Integration with n8n

## 📘 Overview
The **Nanobana Integration with n8n** workflow connects **Google’s Gemini 2.5 Flash API** to n8n, enabling seamless **text-to-image generation** directly from chat input.  

Whenever a message is received through n8n’s Chat Trigger, this workflow sends the input to the Gemini model, retrieves the AI-generated image, and converts it into a downloadable binary file — creating a complete automation loop from prompt to picture.

This setup showcases how **n8n** can integrate with **Google’s generative AI** to power custom creative automation systems.

---

## 🧩 Features
- 🧠 **AI Image Generation:** Generate detailed images from text prompts using Google Gemini 2.5 Flash.  
- ⚡ **Event-Based Automation:** Triggered automatically when a chat message is received.  
- 🪄 **Native API Integration:** Uses Gemini’s REST API through n8n’s built-in HTTP Request node.  
- 🗂️ **Binary File Output:** Converts base64 image data into a ready-to-download image file.  
- 🧱 **Expandable Design:** Can easily connect to Telegram, Slack, or other delivery systems.

---

## 🧠 Workflow Structure

### 🔹 **Nodes Overview**
1. **When Chat Message Received** —  
   Acts as the entry point for user prompts via the Chat Trigger node.

2. **HTTP Request** —  
   Sends the chat input to **Google’s Gemini API** endpoint with your API key.  
   The text prompt is embedded inside the JSON body for image generation.

3. **Convert to File** —  
   Extracts the image data from Gemini’s response (in base64 format)  
   and converts it into a binary image file that n8n can handle natively.

---

## ⚙️ Configuration

### 🔑 **Setup Steps**
1. **Import Workflow:**  
   Import the JSON file `Nanobana_Integration_with_n8n.json` into your n8n instance.

2. **Get Your Gemini API Key:**  
   - Visit [Google AI Studio](https://aistudio.google.com/app/apikey)  
   - Create or use an existing API key for Gemini.  
   - Replace the placeholder in the **HTTP Request** node URL:
     ```bash
     https://generativelanguage.googleapis.com/v1beta/models/gemini-2.5-flash-image-preview:generateContent?key=YOUR_API_KEY
     ```

3. **Customize Input (Optional):**  
   Modify the Chat Trigger or connect an external input (e.g., Telegram or REST API).

4. **Activate the Workflow:**  
   Turn it on in n8n to start generating images in response to chat messages.

---

## 🚀 Run the Workflow
1. Send a message (like *“A neon cyberpunk city at night”*) through your chat interface.  
2. The workflow passes this text to Gemini’s image model.  
3. Gemini generates a visual response.  
4. The **Convert to File** node saves it as a binary image ready for download or sharing.

---

## 🧱 Possible Extensions
- 🔗 Integrate with **Telegram**, **Slack**, or **Discord** to share generated images instantly.  
- ☁️ Save outputs to **Google Drive**, **Dropbox**, or **S3**.  
- 🧰 Chain with other AI nodes (e.g., caption generators or style transformers).  
- 💬 Add user prompts through **n8n Chat UI** for interactive creativity.

---

## ⚖️ Privacy & Compliance
- Uses **Google’s Gemini API** — data sent is processed under Google’s AI terms.  
- No user data is stored permanently by this workflow.  
- For privacy-sensitive use cases, consider disabling execution data storage in n8n.

---

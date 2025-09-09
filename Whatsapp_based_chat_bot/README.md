# WhatsApp-Based Chatbot 🤖
This file contains n8n workflow for a simple WhatsApp chatbot. It uses the WhatsApp Business Cloud API to receive messages and an AI Agent powered by OpenAI to generate responses.

## Features ✨
- **Automated Responses:** Automatically replies to incoming WhatsApp messages. 💬

- **AI-Powered:** Uses the OpenAI gpt-4o-mini model for natural language understanding and response generation. 🧠

- **Contextual Memory:** Maintains a conversation history for each user to provide more relevant and coherent replies. 🧠💡
---
## Prerequisites 🛠️
To use this workflow, you will need:

- An active n8n instance (either self-hosted or cloud). ☁️

- A WhatsApp Business Account with access to the WhatsApp Business Cloud API. 📱

- An OpenAI API Key. 🔑 You can visit [Open AI](https://platform.openai.com/docs/overview) for API keys.

## Setup Instructions 🚀
Import the n8n Workflow:

- Open your n8n instance and create a new workflow.

- Click on the "Import from File" option and upload the JSON file from this repository. 📁

- Configure Credentials:

- WhatsApp Trigger: Set up your WhatsApp Business Cloud API credentials and configure the webhook URL in your Meta for Developers dashboard. 🔗

- OpenAI Chat Model: Provide your OpenAI API Key by creating a new credential. 📝

- WhatsApp Business Cloud: Enter your Phone Number ID and create a new credential for your WhatsApp Business Cloud access token. 📞

- Activate the Workflow: After configuring all the nodes and credentials, save the workflow and activate it to start listening for messages. ▶️

## How it Works 🤔
1. A message from a user triggers the WhatsApp Trigger node.

2. The message content and user's phone number are passed to the AI Agent node. ➡️

3. The AI Agent uses the OpenAI Chat Model to process the message and generate a response. ✨

4. The Simple Memory node maintains the conversation context for a better user experience. 💾

5. Finally, the WhatsApp Business Cloud node sends the AI-generated response back to the user. 📤
---
## Workflow Visualization 🖼️
The workflow is structured as follows:


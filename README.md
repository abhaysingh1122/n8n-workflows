# n8n Workflows
This repository contains a collection of various n8n workflows designed to automate and streamline different processes. Each workflow is a self-contained solution, handling everything from data ingestion and analysis to general automation tasks. The goal is to provide a central hub for reusable and customizable workflows.

## Workflows
This repository contains the following n8n workflows:

- **🌐Vector database creator and analyser:**
    - **Description:** This dual-part workflow automates the process of creating and analyzing a vector database. It ingests documents from Google Drive, converts them into a searchable format in Pinecone, and then uses an AI model to answer user queries based on the stored data.

    - **Files:**
  
      * [Google_Drive_TO_Pinecone_Ingestion](Vector_database_creator_and_analyser/Google_Drive_TO_Pinecone_Ingestion)
      
      * [Vector_Database_Analyst_Workflow](Vector_database_creator_and_analyser/Vector_Database_Analyst_Workflow)
- **🤖 WhatsApp-Based Chatbot:**
      -**Description:** This workflow creates a simple chatbot that receives messages from WhatsApp, processes them using an AI agent powered by OpenAI's ```gpt-4o-mini``` model, and sends a response back to the user.
  
    -**Files:**
      * [whatsapp_chatbot_workflow](Whatsapp_based_chat_bot)
---   
## 🛠️ How to Use
- Clone the Repository: 💻 Clone this repository to your local machine.

- Import Workflows: 📥 Import the .json files for each workflow into your n8n instance.

- Configure Credentials: 🔑 Update the credentials for your Google Drive, Pinecone, and OpenAI accounts within each workflow.

- Activate Workflows:▶️ Activate the workflows in n8n to begin processing documents and answering queries.

## 🤝 Contributing
Feel free to open an issue or submit a pull request if you have suggestions for improvements or new features.

## ❓ Support
If you encounter any issues or have questions about using these workflows, please open an issue in this repository.



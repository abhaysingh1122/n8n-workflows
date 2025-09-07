# Vector database creater and analyser

## Overview
This workflow automates the process of preparing documents for AI analysis.  
It watches a Google Drive folder for new files, processes them into smaller chunks, converts them into vector embeddings, and stores them inside **Pinecone Vector Database**.  

## Why this workflow?
- Instead of manually uploading and preparing data, this workflow automatically ingests any new file added to Google Drive.  
- Files are split into chunks for better semantic search.  
- Embeddings are stored in Pinecone, making later queries efficient and accurate.  

---

# Workflow 1: Google Drive To Pinecone Ingestor.md
This workflow automates the process of ingesting documents from Google Drive and preparing them for analysis.

## How It Works
- Source: The workflow is triggered whenever a new file is added to a specific folder in Google Drive.

- Download: The newly created file is automatically downloaded.

- Get Info: A text splitter extracts text from the document and breaks it into smaller, more manageable chunks.

- Embedder: Each text chunk is converted into a numerical vector using an embeddings model. This process allows for semantic search, meaning the system can understand the meaning of your query rather than just matching keywords.

- Store in Pinecone: The final vector embeddings are saved in your Pinecone vector database. This creates a high-performance index of your documents, ready for fast and accurate retrieval.
---

# Workflow 2: VectorDatabaseAnalyzer.md
This workflow uses the indexed data from the first workflow to answer questions and provide analysis.

## How It Works
- AI Chat Trigger: The process begins when you ask a question in the chat interface.

- AI Analyst: The AI analyst determines what information is needed to answer your query.

- Vector Retrieval: The system uses your question to perform a search in the Pinecone vector database, pulling out the most relevant document chunks (based on their vector similarity).

- Contextual AI: These retrieved chunks are provided as context to a large language model. This model then generates a comprehensive and accurate answer based on the specific information found in your documents.

- Session Memory: The workflow also includes a memory component to remember previous questions and provide better, more coherent answers throughout the conversation.
---
## Notes
- Credentials (Google Drive, OpenAI, Pinecone) are **not included**. Set these up manually in your n8n instance.  
- Works best with text-heavy documents (PDFs, Word, etc.).

## Workflow Diagram
- **Workflow 1 (Google Drive to Pinecone Ingestion):** 
<img width="1540" height="791" alt="Screenshot 2025-09-07 225329" src="https://github.com/user-attachments/assets/707a85f8-a715-4741-a3aa-7ec877a2e9e4" />

- **Workflow 2 (Vector Database Analyst Workflow):** 
<img width="1301" height="783" alt="Screenshot 2025-09-07 225315" src="https://github.com/user-attachments/assets/ac7af864-394e-4341-aacb-c0cf21a309de" />


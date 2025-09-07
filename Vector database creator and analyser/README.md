# Vector database creater and analyser

## Overview
This workflow automates the process of preparing documents for AI analysis.  
It watches a Google Drive folder for new files, processes them into smaller chunks, converts them into vector embeddings, and stores them inside **Pinecone Vector Database**.  

## Why this workflow?
- Instead of manually uploading and preparing data, this workflow automatically ingests any new file added to Google Drive.  
- Files are split into chunks for better semantic search.  
- Embeddings are stored in Pinecone, making later queries efficient and accurate.  

---

## Workflow 1: Google Drive To Pinecone Ingestor.md
This workflow automates the process of ingesting documents from Google Drive and preparing them for analysis.

How It Works
Source: The workflow is triggered whenever a new file is added to a specific folder in Google Drive.

Download: The newly created file is automatically downloaded.

Get Info: A text splitter extracts text from the document and breaks it into smaller, more manageable chunks.

Embedder: Each text chunk is converted into a numerical vector using an embeddings model. This process allows for semantic search, meaning the system can understand the meaning of your query rather than just matching keywords.

Store in Pinecone: The final vector embeddings are saved in your Pinecone vector database. This creates a high-performance index of your documents, ready for fast and accurate retrieval.

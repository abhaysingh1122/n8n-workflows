# Vector database creater and analyser

## Overview
This workflow automates the process of preparing documents for AI analysis.  
It watches a Google Drive folder for new files, processes them into smaller chunks, converts them into vector embeddings, and stores them inside **Pinecone Vector Database**.  

## Why this workflow?
- Instead of manually uploading and preparing data, this workflow automatically ingests any new file added to Google Drive.  
- Files are split into chunks for better semantic search.  
- Embeddings are stored in Pinecone, making later queries efficient and accurate.  

---


# rag-chatbot-n8n
# 🤖 RAG Workflow using n8n

## 🚀 Overview

This project implements a **Retrieval-Augmented Generation (RAG) system** using n8n workflows.
It processes documents from Google Drive, stores embeddings in a vector database, and retrieves relevant information to generate responses using LLMs.

The system is designed as a two-step pipeline:

* Data Ingestion (Google Drive → Pinecone)
* Data Retrieval (Query → Response Generation)

---

## 🔄 Workflows

### 📥 1. Data Storing Workflow

This workflow handles document ingestion and storage.

**Key Functions:**

* Downloads PDF document from Google Drive
* Extracts and processes document content
* Generates embeddings using OpenAI
* Stores embeddings in Pinecone vector database

📄 File: `rag-data-storing-workflow.json`

---

### 💬 2. Data Fetching Workflow

This workflow retrieves relevant data and generates responses.

**Key Functions:**

* Triggered manually or via webhook/API
* Converts query into embeddings
* Retrieves relevant context from Pinecone
* Generates response using OpenAI LLM

📄 File: `rag-data-fetching-workflow.json`

---

## 🛠 Tech Stack

* n8n (Workflow Automation)
* OpenAI API (Embeddings + LLM)
* Pinecone (Vector Database)
* Google Drive API (Document Source)
  
---

## ⚙️ Features

* End-to-end RAG pipeline implementation
* Automated document ingestion from Google Drive
* Vector similarity search using Pinecone
* LLM-based response generation
* Modular workflow design (separate ingestion & retrieval)

---

## 📸 Screenshots



---

## ▶️ How to Run Locally

1. Install n8n
2. Import both workflow files:

   * `rag-data-storing-workflow.json`
   * `rag-data-fetching-workflow.json`
3. Configure credentials:

   * OpenAI API
   * Pinecone API
   * Google Drive access
4. Run the data storing workflow (to ingest document)
5. Trigger fetching workflow manually or via webhook

---

## 🔐 Credentials Setup

This project uses n8n's built-in **Credentials system**.

Before running:

* Add OpenAI API key
* Add Pinecone API key
* Configure Google Drive credentials

⚠️ Note: Credentials are not included for security reasons.

---

## 📌 Limitations

* Uses a **single sample PDF from Google Drive**
* No frontend/UI for user interaction
* Query execution is manual or via API trigger

---

## 💡 Future Improvements

* Add UI for user query input
* Support multiple document ingestion
* Deploy workflow online
* Improve retrieval accuracy

---

## ✨ Key Highlights

* Complete RAG pipeline using n8n
* Integration with Google Drive and Pinecone
* Separation of ingestion and retrieval workflows
* Secure credential management
* Real-world document-based AI system

---

## 👨‍💻 Author

Rishita Goswami


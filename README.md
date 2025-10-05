<div align="center">

# 🧠 Sarathi: A LangGraph RAG Chatbot

**A showcase repository for an advanced, RAG-powered conversational AI built with LangGraph and Streamlit.**

</div>

<div align="center">

[![Live Demo on Hugging Face Spaces](https://img.shields.io/badge/🤗-Live%20Demo%20on%20Hugging%20Face-yellow)](https://huggingface.co/spaces/aryan195a/LangGraph-RAG-Chatbot)
[![Source Code on Hugging Face](https://img.shields.io/badge/💻-Source%20Code%20on%20Hugging%20Face-blue)](https://huggingface.co/spaces/aryan195a/LangGraph-RAG-Chatbot/tree/main)

</div>

---

**Note:** This GitHub repository is for demonstration purposes. The complete, up-to-date source code and the interactive application are hosted on Hugging Face Spaces.

## ✨ Project Overview

Sarathi is an AI guide designed to provide contextual knowledge by answering questions from user-uploaded documents (`.pdf` or `.txt`). It leverages a stateful graph architecture to intelligently handle conversational flow, switching between a document-aware RAG (Retrieval-Augmented Generation) mode and a general chat mode.

## 🚀 Key Features

-   **Dual LLM Backends:** Seamlessly switch between the lightning-fast Groq API (`x-ai/grok-4-fast`) and Google's powerful Gemini (`gemini-2.0-flash`).
-   **Stateful Graph Architecture:** Built with LangGraph for a robust, multi-step, and stateful conversational flow that intelligently routes tasks.
-   **Advanced RAG Pipeline:** Utilizes LlamaIndex and `sentence-transformers` for efficient document chunking, embedding, and retrieval.
-   **Intelligent Context Creation:** Employs a custom strategy to select the most relevant document chunks based on position and keyword relevance, maximizing context quality.
-   **Dynamic Chat Modes:** Automatically switches between a document-aware RAG mode and a general chat mode based on whether a file is uploaded.
-   [cite_start]**Dockerized & Deployable:** Comes with a `Dockerfile` for easy deployment on platforms like Hugging Face Spaces. [cite: 3]

## 🛠️ Technology Stack

| Component         | Technology/Library                                         |
| ----------------- | ---------------------------------------------------------- |
| **Orchestration** | `langgraph`, `langchain`                          |
| **LLM Backends** | `Grok via OpenRouter`, `Google Gemini`               |
| **Retrieval/RAG** | `llama-index`                                     |
| **Embeddings** | `sentence-transformers`                           |
| **Frontend** | `streamlit`                                      |
| **File Parsing** | `pypdf`                                          |

## ⚙️ How It Works

Sarathi uses a graph-based structure to manage the conversation flow. When a query is received, the graph determines the best path:

1.  **Router Node:** Checks if a document retriever is active.
2.  **RAG Path:** If a document is loaded, the graph retrieves relevant chunks and generates an answer based on that context.
3.  **General Chat Path:** If no document is loaded, the graph engages in a standard conversational exchange.

---

<div align="center">

### 🔗 Explore the Project on Hugging Face

[**▶️ Try the Live Demo**](https://huggingface.co/spaces/aryan195a/LangGraph-RAG-Chatbot) | [**📄 View the Source Code**](https://huggingface.co/spaces/aryan195a/LangGraph-RAG-Chatbot/tree/main)

</div>

# Research Assistant Chatbot

A local, privacy-respecting chatbot that helps researchers explore academic papers through Retrieval-Augmented Generation (RAG). Given one or more seed papers, the app builds a knowledge base of related papers (citations and cited-by) and allows the user to ask deep, research-oriented questions like:

> "Has anyone ever applied method X to domain Y?"  
> "What are the main evaluation metrics used for topic Z?"  
> "Is there a consensus on problem P?"

---

## 🧠 Features

- 🧾 Fetches related papers using citation networks
- 📥 Downloads and parses PDFs automatically
- 🧩 Segments paper text into retrievable chunks
- 🔍 Stores embeddings in a vector database (FAISS)
- 💬 Answers user questions using a local LLM via RAG (Ollama)
- 🎛️ Optional filtering by author, year, keywords, and more
- 📊 Visualizes the citation network
- ⚙️ 100% local, free, and open source

---

## 🚀 Quickstart

### 1. Clone the repo

```bash
git clone https://github.com/your-username/research-assistant-chatbot.git
cd research-assistant-chatbot

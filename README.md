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
```

### 2. Install dependencies

```bash
python -m venv venv
source venv/bin/activate   # or .\venv\Scripts\activate on Windows
pip install -r requirements.txt
```

### 3. Start the app

```bash
streamlit run app/ui.py
```

### 4. Requirements
- Python 3.9+
- Ollama installed with a local LLM (e.g. `mistral`, `llama3`)
- Basic tools like `pdftotext` or `pdfminder` if using CLI PDF parsing

## 🧱 Project Structure

```pgsql
app/
├── main.py               ← Entry point for CLI (optional)
├── ui.py                 ← Streamlit interface
├── paper_loader.py       ← Citation retrieval + PDF downloader
├── chunking.py           ← Splits papers into text chunks
├── embedding.py          ← Embeds chunks and stores them in vector DB
├── rag_pipeline.py       ← Handles retrieval and LLM response generation
└── utils.py              ← Helper functions

data/
├── raw_papers/           ← Downloaded PDFs
├── metadata.jsonl        ← Cached paper metadata
└── chunks/               ← Parsed and chunked text segments

vector_db/
├── faiss_index/          ← FAISS vector store
└── chunk_metadata.json   ← Mapping of chunks to papers
```


---

## 🧪 Example Use Cases

- “Has anyone applied transformer models to supply chain optimization?”
- “Which papers cited both [Author A] and [Author B]?”
- “What techniques are most common for domain adaptation in NLP?”

---

## 📖 License

This project is licensed under the MIT License – see the [LICENSE](./LICENSE) file for details.

---

## 🙋‍♀️ Contributing

Pull requests are welcome! If you’d like to suggest a feature or fix a bug, please open an issue first.

---

## 📫 Contact

Built by [Ido Guy](mailto:redrhig@gmail.com)  
Feel free to reach out for collaboration or feedback.

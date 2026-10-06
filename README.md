# 🎥 YouTube Video RAG Assistant

## 🎬 Title & Description
YouTube Video RAG Assistant is an advanced Retrieval-Augmented Generation (RAG) system for extracting and querying knowledge from YouTube videos. It transcribes long-form video audio, processes and indexes the content into a local vector store, and enables context-aware Q&A over the video's content. This project was customized and optimized by **Moayad Fawzi Al-Shumairi** to utilize local vector storage instead of cloud-based vector databases.

## ✨ Key Enhancements & Features
- **Local Vector Database:** Migrated from Pinecone to **ChromaDB** for secure, local, and cost-free embedding storage.
- **Automated Transcription:** Uses OpenAI **Whisper** to convert audio from YouTube videos into accurate text transcripts.
- **Intelligent Chunking:** Implements LangChain's `RecursiveCharacterTextSplitter` to handle very large transcripts (e.g., multi-hour videos) without hitting model token limits.
- **Context-Aware Q&A:** Powered by `GPT-3.5-Turbo` and `OpenAIEmbeddings` to generate precise, low-hallucination answers strictly based on the provided video content.

## 🧰 Tech Stack
- Python 3
- LangChain
- OpenAI API
- ChromaDB (Local)
- Whisper
- PyTube

## ⚙️ Setup & Installation

1. Clone the repository and change into it:
```bash
git clone https://github.com/Moayadai/youtube-rag.git
cd youtube-rag
```

2. Set up a virtual environment and activate it:
```bash
python3 -m venv .venv
source .venv/bin/activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Environment Variables
Create a `.env` file in the project root and add your OpenAI API key:
```text
OPENAI_API_KEY=your_openai_api_key_here
```

> Note: This repository uses ChromaDB for local vector storage, so no external vector DB credentials are required.

## ▶️ Usage
Open and run the Jupyter Notebook `rag.ipynb`. In the notebook:
1. Paste any YouTube video URL into the designated cell.
2. Run the cells to download audio, transcribe with Whisper, chunk and embed the transcript, and build the local ChromaDB index.
3. Once processing completes, use the notebook's Q&A cells to ask questions — the assistant will answer using only the indexed video content.

## 📜 Credits
- **Architecture Optimization & Development:** Moayad Fawzi Al-Shumairi
- **Original Inspiration:** Underfitted

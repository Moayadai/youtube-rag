
```markdown
# 🎥 YouTube Video RAG Assistant

An advanced Retrieval-Augmented Generation (RAG) system that extracts, processes, and queries knowledge directly from lengthy YouTube videos.

This project was customized and optimized by **Moayad Fawzi Al-Shumairi** to utilize local vector storage, eliminating the need for external cloud-based vector databases like Pinecone.

## 🚀 Key Enhancements & Features
*   **Local Vector Database:** Migrated from Pinecone to **ChromaDB** for secure, local, and cost-free embedding storage.
*   **Automated Transcription:** Uses OpenAI's **Whisper** model to convert audio from any YouTube video into highly accurate text transcripts.
*   **Intelligent Chunking:** Implements LangChain's `RecursiveCharacterTextSplitter` to handle massive transcripts (e.g., 3+ hour videos) without hitting AI token limits.
*   **Context-Aware Q&A:** Powered by `GPT-3.5-Turbo` and `OpenAIEmbeddings` to generate precise, hallucination-free answers based *strictly* on the provided video content.

## 🛠️ Tech Stack
*   **Core:** Python 3
*   **Orchestration:** LangChain
*   **LLM & Embeddings:** OpenAI API
*   **Vector Database:** ChromaDB (Local)
*   **Audio Processing:** Whisper, PyTube

## ⚙️ Setup & Installation

**1. Clone the repository:**
```bash
git clone https://github.com/Moayadai/youtube-rag.git
cd youtube-rag

```

**2. Set up the virtual environment:**

```bash
python3 -m venv .venv
source .venv/bin/activate

```

**3. Install dependencies:**

```bash
pip install -r requirements.txt

```

**4. Environment Variables:**
Create a `.env` file in the root directory. Since this version uses ChromaDB, you only need to provide your OpenAI API key:

```text
OPENAI_API_KEY=your_openai_api_key_here

```

## 💡 Usage

Run the Jupyter Notebook (`rag.ipynb`) to initialize the system interactively. Provide any YouTube URL in the designated cell, wait for the transcription and embedding process, and start asking questions about the video's content!

## 📜 Credits

* **Architecture Optimization & Development:** Moayad Fawzi Al-Shumairi.
* **Original Inspiration:** This project builds upon the foundational RAG concepts presented by *Underfitted*, significantly modified for local database execution and streamlined performance.

```

```

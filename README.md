# genai-rag-chatbot

### Ask Me Anything – RAG Chatbot using LangChain + OpenAI/Hugging Face

This is a lightweight Retrieval-Augmented Generation (RAG) chatbot that takes a document (e.g., PDF) and answers questions using LangChain, FAISS, and either OpenAI or Hugging Face Transformers.

---

###  Objective

- Load and chunk a PDF or plain text file
- Store embeddings in a vector database (FAISS)
- Retrieve relevant context on a query
- Generate answers using a Language Model (OpenAI GPT or HF model)

---

###  Tech Stack

- Python 3.10+
- [LangChain](https://github.com/hwchase17/langchain) – LLM chaining and orchestration
- [FAISS](https://github.com/facebookresearch/faiss) – Local vector store for retrieval
- [OpenAI SDK](https://platform.openai.com/docs/) or [Hugging Face Transformers](https://huggingface.co/docs/transformers/) – For generating responses
- [PyMuPDF](https://pymupdf.readthedocs.io/) – For PDF text extraction
- [Gradio](https://gradio.app/) – (Optional) for building a lightweight UI

---

###  Virtual Environment Setup (macOS/Homebrew Python)

 Recommended: Do **not** install packages globally if you're using Homebrew Python. Use a virtual environment instead.

### 1. Create and activate a virtual environment:
```bash
python3 -m venv .venv
source .venv/bin/activate

### 2. Install dependencies:
pip install langchain faiss-cpu openai transformers PyMuPDF gradio


### What these packages do:
Package	Purpose
langchain	Framework for chaining LLMs with memory, tools, and retrievers
faiss-cpu	Fast vector similarity search for embedding-based retrieval
openai	API client to access OpenAI models like GPT-3.5, GPT-4
transformers	Hugging Face library to use models like BERT, GPT-2, Falcon, etc.
PyMuPDF	Parses PDF content for document Q&A pipelines
gradio	Creates a browser-based UI for chatbot interaction

File Structure:
.
├── data/
│   └── my_resume.pdf
├── app.py
├── .env
└── README.md

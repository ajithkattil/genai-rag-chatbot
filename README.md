# genai-rag-chatbot

# 🧠 Ask Me Anything – RAG Chatbot using LangChain + OpenAI/Hugging Face

This is a lightweight Retrieval-Augmented Generation (RAG) chatbot that takes a document (e.g., PDF) and answers questions using LangChain, FAISS, and either OpenAI or Hugging Face Transformers.

## 🚀 Objective

- Load and chunk a PDF or plain text file
- Store embeddings in a vector database (FAISS)
- Retrieve relevant context on a query
- Generate answers using a Language Model (OpenAI GPT or HF model)

---

## 🛠️ Tech Stack

- Python 3.10+
- [LangChain](https://github.com/hwchase17/langchain)
- [FAISS](https://github.com/facebookresearch/faiss)
- [OpenAI SDK](https://platform.openai.com/docs/) or [Hugging Face Transformers](https://huggingface.co/docs/transformers/)
- [Gradio](https://gradio.app/) (optional UI)

---

## 📦 Installation

```bash
pip install langchain faiss-cpu openai transformers PyMuPDF gradio

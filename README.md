
# GenAI RAG Chatbot

## GenAI RAG Chatbot – Resume Q&A with LangChain + OpenAI + Gradio

This is a Retrieval-Augmented Generation (RAG) chatbot that lets you ask questions about your own documents (like a resume PDF) using OpenAI’s GPT-3.5 Turbo and LangChain. It processes a PDF, embeds it using OpenAI Embeddings, stores it in a FAISS vector index, and serves a local Gradio web app for conversational querying.

##  Features

- Load and split PDFs
- Generate embeddings via OpenAI
- Store vectors locally using FAISS
- Use GPT-3.5 Turbo for answering questions
- Simple Gradio web UI

##  Prerequisites

- macOS with Python 3.12+ (preferably installed via Homebrew)
- OpenAI account with API key and billing enabled
- Basic terminal usage

##  Global Installation (No Virtual Environment Needed)

python3 -m pip install --break-system-packages \
  langchain \
  langchain-community \
  langchain-openai \
  pymupdf \
  pypdf \
  openai \
  gradio \
  sentence-transformers \
  faiss-cpu \
  python-dotenv


##  Set Up OpenAI API Key

Create a .env file in the project root:
touch .env

Add your OpenAI API key to it:
OPENAI_API_KEY=sk-xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx

Your OpenAI account must have billing enabled or remaining credits.

## 📁 Folder Structure

genai-rag-chatbot/  
├── app.py                → Main application script  
├── .env                  → OpenAI API key (not committed to git)  
├── data/  
│   └── my_resume.pdf     → Your resume or any PDF document  
└── README.md             → This file

## ▶️ Run the App

Run the chatbot locally:
python3 app.py

Then open your browser and go to:
http://127.0.0.1:7860

## 💸 Cost Estimate (OpenAI API)

Embeddings (text-embedding-ada-002): $0.0001 per 1K tokens
GPT-3.5-Turbo Input: $0.0015 per 1K tokens
GPT-3.5-Turbo Output: $0.002 per 1K tokens
Typical Session: ~$0.01–$0.05

To avoid embedding costs, see the Hugging Face option below.

## 🧠 Optional: Use Free HuggingFace Embeddings

Replace this in app.py:
from langchain_openai import OpenAIEmbeddings
embedding_model = OpenAIEmbeddings()

With:
from langchain_community.embeddings import HuggingFaceEmbeddings
embedding_model = HuggingFaceEmbeddings(model_name="all-MiniLM-L6-v2")

Then install:
python3 -m pip install --break-system-packages sentence-transformers

## 🔄 LangChain v0.2+ Compatibility Notes

LangChain split its functionality into langchain-community and langchain-openai. This project uses the updated imports:
from langchain_community.document_loaders import PyPDFLoader
from langchain_community.vectorstores import FAISS
from langchain_community.chat_models import ChatOpenAI
from langchain_openai import OpenAIEmbeddings

=======
---
title: Genai Rag Chatbot
emoji: 📊
colorFrom: indigo
colorTo: purple
sdk: gradio
sdk_version: 5.39.0
app_file: app.py
pinned: false
short_description: GenAI RAG Chatbot – Sample Document Q&A with LangChain + Ope
---

Check out the configuration reference at https://huggingface.co/docs/hub/spaces-config-reference
>>>>>>> a8b7197d073066b2b01975403d9e5d5784b99377

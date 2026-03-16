# semantic-rag-chatbot
# Semantic RAG Chatbot

This project implements a Retrieval-Augmented Generation style chatbot
using semantic chunking and embedding similarity.

## Features
- Semantic chunking
- SentenceTransformer embeddings
- Cosine similarity search
- Threshold-based hallucination prevention

## Tech Stack
- Python
- LangChain
- Sentence Transformers
- Scikit-learn

## How it Works
1. Text is split using semantic chunking
2. Embeddings are created
3. User query is embedded
4. Cosine similarity finds best chunk
5. Bot returns relevant answer

## Run

pip install -r requirements.txt
python chatbot.py

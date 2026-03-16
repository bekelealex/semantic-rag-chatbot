# Upwork Policy Semantic RAG Chatbot

## Overview

This project is a simple **semantic RAG-style chatbot** that answers questions about an Upwork guide document. The goal of the project is to demonstrate how a chatbot can search through a document and return relevant information based on a user's question.

Instead of relying on basic keyword matching, the chatbot uses **semantic embeddings and vector search** to understand the meaning behind questions. This allows it to find the most relevant sections of the document even when the wording of the question is different from the original text.

The chatbot reads a structured text file (`upwork_guide.txt`) that contains information about how Upwork works, including topics such as creating an account, how freelancers apply for jobs, how clients post projects, and general platform policies.

---

## How the Chatbot Works

The system follows a simple retrieval-based process.

First, the Upwork guide document is loaded and split into smaller pieces using **semantic chunking**. These chunks are created based on meaning rather than fixed character length, which helps preserve the context of each section.

Next, each chunk is converted into a numerical representation called an **embedding** using the `all-MiniLM-L6-v2` model. These embeddings are then stored in a **FAISS vector database**.

When a user asks a question, the system converts the question into an embedding and searches the vector database to find the most similar chunks from the document. The most relevant sections are then returned as the response.

---

## Main Features

This project includes several important features:

* Semantic document chunking
* Embedding generation using sentence transformers
* Vector similarity search with FAISS
* Retrieval of relevant document sections
* A simple interactive chatbot interface in the terminal

These components together demonstrate the core idea behind **Retrieval-Augmented Generation (RAG)** systems.

---

## Project Structure

```text
project-folder/

rag_chatbot.py
upwork_guide.txt
requirements.txt
README.md
```

* **rag_chatbot.py** contains the chatbot logic.
* **upwork_guide.txt** is the knowledge base used by the chatbot.
* **requirements.txt** lists the required Python dependencies.
* **README.md** explains the project and how to run it.

---

## Installation

Before running the chatbot, install the required Python packages:

```
pip install langchain
pip install langchain-community
pip install langchain-experimental
pip install langchain-huggingface
pip install sentence-transformers
pip install faiss-cpu
pip install transformers
```

---

## Running the Chatbot

After installing the dependencies, run the chatbot with:

```
python rag_chatbot.py
```

Once the program starts, you can ask questions related to the Upwork guide.

Example questions:

* How do I create an account on Upwork?
* How do freelancers apply for jobs?
* What is escrow payment?
* How do clients post a project?

To exit the chatbot, simply type:

```
exit
```

---

## Purpose of This Project

The main purpose of this project is to demonstrate how a **basic document-based question answering system** can be built using modern AI tools.

It serves as a learning project for understanding key RAG concepts such as:

* semantic chunking
* embeddings
* vector databases
* similarity search

---

## Possible Future Improvements

There are several ways this project could be expanded in the future. For example:

* Integrating a large language model to generate more natural answers
* Building a web interface using Streamlit
* Allowing the chatbot to read multiple documents
* Adding conversation memory for better interactions

These improvements would make the chatbot more powerful and closer to real-world AI applications.

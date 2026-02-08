# Project Context-Engine  
## Building a Proprietary Knowledge Retrieval Pipeline using Naive RAG

---

## 1. Introduction

Large Language Models (LLMs) are powerful, but they cannot reliably answer questions about **private or unseen data**.  
**Retrieval-Augmented Generation (RAG)** solves this by retrieving relevant information from a private corpus and injecting it into the model’s prompt.

In this project, we build a **Naive RAG pipeline** that answers questions using a single private ebook from Project Gutenberg.

---

## 2. Objective

The goal of this project is to:

- Build a simple Retrieval-Augmented Generation (RAG) system
- Use a private document that the model was not trained on
- Retrieve relevant text chunks for a user query
- Generate answers grounded only in the retrieved context

---

## 3. Dataset

- **Source**: Project Gutenberg  
- **eBook ID**: 55695  
- **URL**: https://www.gutenberg.org/ebooks/55695  
- **Format**: Plain text (`.txt`)

This ebook acts as the **private knowledge base** for the system.

---

## 4. What is Naive RAG?

A **Naive RAG pipeline** is the most basic form of Retrieval-Augmented Generation and consists of four core steps:

1. Document Loading  
2. Text Chunking  
3. Embedding & Vector Storage  
4. Retrieval + Answer Generation  

No re-ranking, no memory, no feedback loops—just the fundamentals.

---

## 5. System Architecture
> User Question  
> ↓  
> Query Embedding  
> ↓  
> Vector Similarity Search  
> ↓  
> Top-K Relevant Chunks  
> ↓  
> Prompt Construction  
> ↓  
> LLM Answer



---

## 6. Technology Stack

- Python
- SentenceTransformers (for embeddings)
- Chromadb (vector similarity search)
- LLM (google/flan-t5-base)

---





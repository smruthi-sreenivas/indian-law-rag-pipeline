# indian-law-rag-pipeline

# Indian Laws RAG Pipeline

This project implements a **Retrieval-Augmented Generation (RAG)** pipeline designed to answer **queries related to Indian laws** using **LLMs and optimized retrieval**.

---

## 📘 Objective

To build a system that can accurately retrieve and generate grounded responses from a large corpus of **Indian legal documents**, using **LangChain** and **Cohere / OpenAI models**.

---

## ⚙️ Features

- 📚 Uses **Indian Laws Dataset** (IPC, IT Act, Constitution, etc.)
- 🔍 **Hybrid Retrieval + Reranking** (Cohere Rerank)
- 🧠 **LLM-based answer generation** grounded in law text

---

## 🧰 Tech Stack

- **LangChain**
- **Cohere / OpenAI LLMs**
- **Chroma / FAISS** for vector store
- **BM25 / Reranker** for retrieval optimization

---

## 🚀 Pipeline Flow

1. **Data Loading:** Load Indian Laws dataset into a retriever  
2. **Indexing:** Create embeddings and vector database  
3. **Retrieval:** Use `ContextualCompressionRetriever` with reranker  
4. **RAG Chain:** Combine context + question → prompt → LLM  
5. **Response Generation:** Produce final answer grounded in law text  

---

## 🧪 Evaluation

Since a labeled test set is not available, **manual evaluation** was performed using a curated set of **Indian law questions** covering:

- IPC (Criminal Law)
- IT Act (Cyber Law)
- Indian Contract Act
- Indian Constitution

The pipeline was assessed for:
- **Relevance:** Did it retrieve correct section?  
- **Accuracy:** Is the generated answer legally valid?  
- **Faithfulness:** No hallucinations or fabricated facts  

---


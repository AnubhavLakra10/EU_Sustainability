# EU Green Deal Compliance FAQ Bot

A **Retrieval-Augmented Generation (RAG)** based AI agent that helps SMEs and businesses quickly find answers to common questions about EU Green Deal policies.  
This bot focuses on frequently asked questions (FAQs) related to the most relevant EU environmental regulations, providing short, clear answers to help businesses understand and meet compliance standards.

---

## Functionality
- Answers basic questions about key EU environmental regulations.
- Covers common requirements such as:
  - Waste management
  - Carbon footprint reporting
  - Renewable energy adoption
- Provides **short, clear, and context-aware** responses.

---

## Motivation
Navigating EU Green compliance can be overwhelming for businesses, especially SMEs without dedicated compliance teams.  
This project aims to simplify the process by providing a **smart, accessible FAQ bot** that:
- Delivers instant, accurate answers.
- Reduces the time and effort needed to interpret policies.
- Encourages sustainability through better understanding of regulations.

---

## Method Details

### **1. Document Storage & Embedding**
- Large policy documents are split into **semantic chunks** using an LLM.
- Chunks are stored in a **FAISS vectorstore** for efficient retrieval.

### **2. Query Processing**
- User queries are rephrased to improve clarity.
- Queries are embedded using the same model as the documents.
- Vector similarity search retrieves the **most relevant chunks**.

### **3. Summarization**
- Retrieved chunks are passed to an LLM for **concise, context-aware answers**.
- Responses are tailored to match the user's question precisely.

### **4. Evaluation**
- Answers are compared against a **gold Q&A dataset**.
- Metrics: **Cosine Similarity**, **F1 Score**, and **Semantic Match**.

---

## Key Agents
- **Retriever Agent** – Retrieves the most semantically relevant document chunks.
- **Summarizer Agent** – Generates coherent, concise responses.
- **Evaluation Agent** – Measures factual accuracy & contextual relevance.

---

## Benefits
- **Accuracy & Fact-Checking** – Reduces hallucination by grounding answers in verified documents.
- **Modularity** – Components can be updated independently.
- **Better Evaluation** – Combines quantitative metrics with benchmark datasets.
- **Flexibility** – Easily adaptable to other domains and use cases.
- **Context-Aware Responses** – Uses both query context and retrieved content.

---

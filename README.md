# Multilingual RAG Document Assistant

## Overview
This project demonstrates a Retrieval-Augmented Generation (RAG) system for answering questions from multilingual documents (English + French).

The system retrieves relevant document chunks and generates grounded responses using LLMs, reducing hallucinations and improving reliability.

---

## Problem
Large Language Models often hallucinate when answering questions without context. This is especially critical in document-heavy workflows like policies, contracts, and FAQs.

---

## Solution
Built a multilingual RAG pipeline that:
- Retrieves relevant document chunks
- Generates answers grounded in context
- Detects missing information cases

---

## Tech Stack
- LangChain (for orchestration)
- OpenAI API (LLM responses)
- Vector embeddings (for retrieval)
- Python (basic workflow)

---

## Key Features
- Multilingual support (English + French)
- Context-aware question answering
- Failure detection ("Not found in document")
- Simple evaluation framework

---

## Prompt Strategy
- Strict grounding:
  "Answer ONLY from the provided context."
- Fallback handling:
  "If information is missing, respond with 'Not found in document'."

---

## Evaluation
Created a manual evaluation set of 15 queries:
- Measured correctness of responses
- Identified failure modes:
  - Missing context
  - Partial answers
  - Retrieval errors

---

## Results
- Improved answer reliability
- Reduced hallucinations
- Better handling of multilingual queries

---

## Example Use Case
Upload policy documents → Ask:
"What is the refund policy?"

→ System retrieves relevant section → Generates grounded answer

---

## Future Improvements
- Better chunking strategy
- Add automated evaluation metrics
- Improve cross-lingual retrieval

---

## Author
Jahanvi Saxena 

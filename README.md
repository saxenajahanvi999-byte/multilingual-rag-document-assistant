# Multilingual RAG Document Assistant

## Overview

This project is a multilingual Retrieval-Augmented Generation (RAG) assistant designed to improve factual accuracy in document-based question answering.

Instead of relying only on the model’s internal knowledge, the system retrieves relevant document chunks and generates grounded responses using contextual retrieval.

The project focuses on:
- reducing hallucinations
- multilingual retrieval
- structured AI workflows
- prompt reliability

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

## Project Focus

This project focuses on:
- reducing hallucinations
- retrieval grounding
- multilingual document QA
- structured AI workflows
- prompt reliability

---

## Key Features
- Multilingual support (English + French)
- Context-aware question answering
- Failure detection ("Not found in document")
- Simple evaluation framework

---

## System Workflow

User Query
   ↓
Embedding Generation
   ↓
Vector Search
   ↓
Retrieve Relevant Chunks
   ↓
Prompt + Context Sent to OpenAI API
   ↓
Grounded Response Generated

---

## Why RAG?

Large Language Models can hallucinate or generate unsupported answers when relying only on internal knowledge.

RAG improves reliability by retrieving relevant external context before generation, helping produce more grounded and context-aware responses.

---
## Tech Stack

- Python (Basic)
- OpenAI API
- JSON
- Prompt Engineering
- Retrieval-Augmented Generation (RAG)
- Vector Search Concepts
- GitHub

## Installation

Clone the repository:

```bash
git clone https://github.com/saxenajahanvi999-byte/multilingual-rag-document-assistant.git
```

Navigate to the project directory:

```bash
cd multilingual-rag-document-assistant
```

Install required dependencies:

```bash
pip install -r requirements.txt
```

Set up your OpenAI API key:

```bash
OPENAI_API_KEY=your_api_key
```

## Usage

1. Upload or provide documents for retrieval.
2. The system converts document chunks into embeddings.
3. Relevant chunks are retrieved using vector similarity search.
4. The retrieved context and user query are sent to the OpenAI API.
5. The model generates a grounded response based on retrieved context.

Run the application:

```bash
python app.py
```

Example Query:

```text
What is the refund policy?
```

Example Output:

```text
The refund policy allows returns within 7 days of purchase.
```

## Example Queries / Outputs

### Example 1 — Policy Question

#### User Query
```text
What is the refund policy?
```

#### Retrieved Context
```text
Refunds are allowed within 7 days of purchase with a valid receipt.
```

#### Generated Answer
```text
The refund policy allows returns within 7 days of purchase with a valid receipt.
```

---

### Example 2 — Multilingual Retrieval

#### User Query
```text
What are the delivery timelines?
```

#### Retrieved Context
```text
Les livraisons prennent généralement entre 3 et 5 jours ouvrables.
```

#### Generated Answer
```text
The delivery timeline is typically between 3–5 business days.
```
### Failure Example — Missing Context

#### User Query
```text
What is the international warranty policy?
```

#### Retrieved Context
```text
No relevant context found.
```

#### System Response
```text
The requested information was not found in the provided documents.
```
## Challenges Faced

### 1. Retrieval Accuracy
Retrieving semantically relevant chunks consistently was challenging, especially for multilingual queries.

### 2. Hallucination Control
The model occasionally generated unsupported answers when relevant context was missing.

### 3. Chunking Strategy
Choosing optimal chunk sizes required balancing retrieval relevance and contextual completeness.

### 4. Multilingual Retrieval
Cross-language retrieval performance varied depending on document structure and query phrasing.

These challenges helped improve my understanding of retrieval reliability, prompt grounding, and practical AI workflow design.

## Evaluation
Created a manual evaluation set of 15 queries:
- Measured correctness of responses
- Identified failure modes:
  - Missing context
  - Partial answers
  - Retrieval errors

--

## Future Improvements
- Better chunking strategy
- Add automated evaluation metrics
- Improve cross-lingual retrieval

---

## Current Limitations

- Retrieval quality depends on chunking strategy
- Cross-lingual retrieval can be inconsistent
- Large documents may increase latency
- Responses depend on document quality and coverage

---

## Key Learnings

- Retrieval grounding improves factual reliability
- Chunking strategy affects retrieval quality
- Structured prompting improves consistency
- Failure analysis is important for reliable AI systems
- Multilingual retrieval introduces semantic challenges

---

## 📈 Impact

- Reduced hallucination using structured prompts
- Improved answer reliability via retrieval
- Enabled multilingual query handling

---

## Author
Jahanvi Saxena 

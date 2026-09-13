# 🔬 AI Research Assistant

> An AI-powered research companion for reading, searching, understanding, comparing, and analyzing academic research papers.

![Status](https://img.shields.io/badge/Status-Under%20Development-orange)
![Python](https://img.shields.io/badge/Python-3.11+-blue)
![FastAPI](https://img.shields.io/badge/FastAPI-Backend-009688)
![React](https://img.shields.io/badge/React-Frontend-61DAFB)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-Database-336791)
![pgvector](https://img.shields.io/badge/pgvector-Vector%20Search-purple)
![License](https://img.shields.io/badge/License-MIT-green)

---

## 📌 Overview

**AI Research Assistant** is a full-stack AI application designed to help students, researchers, and professionals analyze academic research papers efficiently.

Users can upload one or multiple research papers in PDF format and interact with them using natural language.

The system combines **Natural Language Processing (NLP), transformer-based embeddings, semantic search, vector databases, Retrieval-Augmented Generation (RAG), and Large Language Models (LLMs)** to provide context-aware and citation-grounded responses.

Instead of manually searching through multiple research papers, users can ask questions, generate summaries, compare papers, extract key information, and explore potential research gaps.

---

## 🎯 Problem Statement

Research papers contain large amounts of technical information distributed across multiple pages and sections.

Students and researchers often spend significant time finding:

- Research objectives
- Methodologies
- Datasets
- Algorithms
- Models
- Evaluation metrics
- Results
- Limitations
- Future work
- Differences between multiple papers
- Potential research gaps

Traditional keyword-based search may fail when the exact words used in a query do not appear in a document.

The **AI Research Assistant** addresses this problem using **semantic search and Retrieval-Augmented Generation (RAG)**.

---

## 💡 Proposed Solution

The application converts uploaded research papers into searchable semantic representations.

The overall workflow is:

```text
Research Paper (PDF)
        ↓
Text Extraction
        ↓
Text Cleaning
        ↓
Section Detection
        ↓
Document Chunking
        ↓
Embedding Generation
        ↓
Vector Database
        ↓
Semantic Retrieval
        ↓
Relevant Context
        ↓
Large Language Model
        ↓
Grounded Answer
        ↓
Citations
```

---

# ✨ Key Features

## 📄 1. Research Paper Upload

Users can upload one or multiple academic papers in PDF format.

Features include:

- PDF upload
- Multiple document support
- Drag-and-drop upload
- File validation
- File size validation
- Duplicate detection
- Document processing status
- Document deletion

---

## 🧠 2. Intelligent Document Processing

Every uploaded paper passes through a structured document-processing pipeline:

```text
PDF
 ↓
Text Extraction
 ↓
Text Cleaning
 ↓
Section Detection
 ↓
Document Chunking
 ↓
Metadata Assignment
 ↓
Embedding Generation
 ↓
Vector Storage
```

The system preserves important metadata including:

- Document ID
- File name
- Page number
- Section name
- Chunk ID

This metadata is later used for source attribution and citation generation.

---

## 🔎 3. Semantic Search

The system uses **semantic search** rather than relying only on exact keyword matching.

For example, a user may ask:

> "Which neural network architecture was used for image classification?"

The system can retrieve a relevant passage such as:

> "The proposed system uses ResNet-50 for classification."

even if the exact wording is different.

This is achieved using **transformer-based embeddings and vector similarity search**.

---

## 🤖 4. Retrieval-Augmented Generation (RAG)

RAG is the core architecture of the AI Research Assistant.

```text
                  ┌───────────────────┐
                  │   User Question   │
                  └─────────┬─────────┘
                            ↓
                  ┌───────────────────┐
                  │  Query Embedding  │
                  └─────────┬─────────┘
                            ↓
                  ┌───────────────────┐
                  │  Vector Search    │
                  └─────────┬─────────┘
                            ↓
                  ┌───────────────────┐
                  │ Relevant Chunks   │
                  └─────────┬─────────┘
                            ↓
                  ┌───────────────────┐
                  │ Context Builder   │
                  └─────────┬─────────┘
                            ↓
                  ┌───────────────────┐
                  │       LLM         │
                  └─────────┬─────────┘
                            ↓
                  ┌───────────────────┐
                  │ Answer + Sources  │
                  └───────────────────┘
```

The system retrieves relevant information from uploaded research papers and provides it as context to the LLM.

The model is instructed to:

- Use retrieved context as the primary source
- Avoid unsupported claims
- Avoid fabricating information
- Clearly indicate when information is unavailable
- Provide relevant citations
- Distinguish information between different papers

---

## 📚 5. Citation-Grounded Answers

A major feature of the project is **source attribution**.

Example:

```text
The proposed model achieved an accuracy of 94.2%.

[Source: Research_Paper.pdf, Page 7]
```

Citations can include:

- Paper name
- Page number
- Section
- Relevant source passage

This makes the generated answers easier to verify against the original research papers.

---

## 📝 6. Research Paper Summarization

The assistant can generate a structured summary of an uploaded research paper.

Instead of reading the entire paper to understand its main contribution, users can quickly obtain:

- Research problem
- Research objective
- Methodology
- Dataset
- Models and algorithms
- Evaluation metrics
- Key results
- Limitations
- Future work

### Example

**User:**  
> Summarize this research paper and explain its main contribution.

**AI Research Assistant:**

```text
📄 Paper Summary

Research Problem:
The paper addresses...

Objective:
The authors aim to...

Methodology:
The proposed approach uses...

Dataset:
The experiments were conducted using...

Model:
The authors used...

Results:
The proposed method achieved...

Limitations:
The study is limited by...

Future Work:
The authors propose...

## 🔬 8. Research Gap Analysis

The system can analyze multiple research papers and identify potential research gaps based on their methodologies, datasets, results, and limitations.

The workflow is:

```text
Multiple Research Papers
          ↓
Methodology Analysis
          ↓
Dataset Analysis
          ↓
Results Analysis
          ↓
Limitations
          ↓
Common Problems
          ↓
Potential Research Gaps
```

The identified gaps are presented as **AI-generated suggestions** and should be verified against the original literature.

---

## 🧩 9. Key Information Extraction

The system can extract important information from research papers, including:

- Research objectives
- Datasets
- Algorithms
- Models
- Evaluation metrics
- Performance values
- Methodologies
- Limitations
- Future work

This allows researchers to quickly understand the technical content of a paper.

---

## 💬 10. Research Chat

Users can interact with uploaded papers through a conversational interface.

Example questions:

```text
What is the main objective of this paper?

What problem does this research solve?

Which dataset was used?

Which model was used?

Explain the methodology.

What evaluation metrics were used?

What performance did the proposed method achieve?

What are the limitations?

What future work did the authors suggest?

Compare these two research papers.

Which paper achieved the best performance?

What potential research gaps can be identified?
```

Planned capabilities include:

- Conversation history
- New conversations
- Suggested questions
- Markdown responses
- Source citations
- Source previews
- Paper selection
- Multi-paper conversations

---

## 📈 11. Research Dashboard

The dashboard provides an overview of the user's research library.

It can display:

- Number of papers
- Total pages
- Total processed chunks
- Recent papers
- Recent conversations
- Most queried papers
- Document processing status

The dashboard focuses on meaningful research information rather than unnecessary visualizations.

---

# 🧠 AI/ML Concepts Used

This project demonstrates practical concepts from Artificial Intelligence, Machine Learning, Natural Language Processing, and Generative AI.

## Natural Language Processing

- Text preprocessing
- Tokenization
- Text chunking
- Semantic representation
- Natural language understanding

## Machine Learning / AI

- Vector representations
- Semantic similarity
- Information retrieval
- Transformer models
- Embeddings
- Similarity ranking
- Retrieval systems

## Generative AI

- Large Language Models
- Retrieval-Augmented Generation
- Prompt engineering
- Context augmentation
- Grounded generation
- LLM evaluation

---

# 🔢 Embedding-Based Retrieval

Research-paper text is converted into numerical vector representations using an embedding model.

```text
Research Text
      ↓
Embedding Model
      ↓
Vector Representation
```

For example:

```text
"Deep learning improves image classification"
                    ↓
        [0.21, -0.08, 0.73, ...]
```

The user's query is also converted into a vector.

The system compares the query vector with stored document vectors to retrieve semantically relevant passages.

---

# 🗄️ Vector Database

The project uses **PostgreSQL with pgvector** for storing and searching embeddings.

Conceptual structure:

```text
PostgreSQL
│
├── Documents
│
├── Document Chunks
│
├── Embeddings
│
├── Conversations
│
└── Messages
```

The vector database enables efficient similarity-based retrieval across uploaded research papers.

---

# 🏗️ System Architecture

```text
┌──────────────────────────────────────────────────────────────┐
│                         FRONTEND                             │
│                    React + TypeScript                        │
│                                                              │
│ Dashboard │ Papers │ Search │ Chat │ Compare │ Evaluation   │
└────────────────────────────┬─────────────────────────────────┘
                             │
                          REST API
                             │
┌────────────────────────────▼─────────────────────────────────┐
│                         BACKEND                              │
│                          FastAPI                             │
│                                                              │
│ API Routes │ Validation │ Services │ Application Logic       │
└───────────────┬─────────────────────────────┬────────────────┘
                │                             │
                ▼                             ▼
┌──────────────────────────┐      ┌────────────────────────────┐
│   DOCUMENT PROCESSING    │      │       AI / ML PIPELINE     │
│                          │      │                            │
│ PDF Extraction           │      │ Embeddings                 │
│ Text Cleaning            │      │ Semantic Retrieval         │
│ Section Detection        │      │ RAG                        │
│ Chunking                 │      │ LLM                        │
│ Metadata Extraction      │      │ Evaluation                 │
└──────────────┬───────────┘      └──────────────┬─────────────┘
               │                                 │
               └────────────────┬────────────────┘
                                ▼
                   ┌─────────────────────────┐
                   │       PostgreSQL         │
                   │        + pgvector        │
                   │                         │
                   │ Documents               │
                   │ Chunks                  │
                   │ Embeddings              │
                   │ Conversations           │
                   │ Messages                │
                   └─────────────────────────┘
```

---

# 🌳 Project Structure

```text
AI-Research-Assistant/
│
├── frontend/
│   ├── public/
│   └── src/
│       ├── components/
│       ├── pages/
│       ├── layouts/
│       ├── hooks/
│       ├── services/
│       ├── types/
│       ├── utils/
│       └── App.tsx
│
├── backend/
│   ├── app/
│   │   ├── api/
│   │   │   ├── routes/
│   │   │   │   ├── documents.py
│   │   │   │   ├── chat.py
│   │   │   │   ├── search.py
│   │   │   │   ├── papers.py
│   │   │   │   └── evaluation.py
│   │   │   └── dependencies.py
│   │   │
│   │   ├── core/
│   │   │   ├── config.py
│   │   │   └── security.py
│   │   │
│   │   ├── database/
│   │   │   ├── connection.py
│   │   │   └── models.py
│   │   │
│   │   ├── schemas/
│   │   │   ├── document.py
│   │   │   ├── chat.py
│   │   │   └── search.py
│   │   │
│   │   ├── services/
│   │   │   ├── document_processing/
│   │   │   │   ├── pdf_parser.py
│   │   │   │   ├── text_cleaner.py
│   │   │   │   ├── section_detector.py
│   │   │   │   └── chunker.py
│   │   │   │
│   │   │   ├── embeddings/
│   │   │   │   └── embedding_service.py
│   │   │   │
│   │   │   ├── retrieval/
│   │   │   │   └── vector_search.py
│   │   │   │
│   │   │   ├── rag/
│   │   │   │   ├── retriever.py
│   │   │   │   ├── context_builder.py
│   │   │   │   └── generator.py
│   │   │   │
│   │   │   ├── analysis/
│   │   │   │   ├── summarizer.py
│   │   │   │   ├── comparator.py
│   │   │   │   └── gap_analyzer.py
│   │   │   │
│   │   │   └── evaluation/
│   │   │       ├── retrieval_eval.py
│   │   │       └── rag_eval.py
│   │   │
│   │   ├── utils/
│   │   └── main.py
│   │
│   └── tests/
│       ├── unit/
│       └── integration/
│
├── ml/
│   ├── notebooks/
│   ├── datasets/
│   ├── experiments/
│   └── evaluation/
│
├── scripts/
│   ├── setup_db.py
│   └── ingest_documents.py
│
├── docs/
│   ├── architecture.md
│   ├── api.md
│   └── evaluation.md
│
├── docker/
│   ├── backend.Dockerfile
│   └── frontend.Dockerfile
│
├── .env.example
├── .gitignore
├── docker-compose.yml
├── requirements.txt
├── package.json
├── LICENSE
└── README.md
```

---

# 🔄 Document Processing Pipeline

```text
                     PDF Upload
                         │
                         ▼
                 ┌───────────────┐
                 │ PDF Validation │
                 └───────┬───────┘
                         ▼
                 ┌───────────────┐
                 │Text Extraction│
                 └───────┬───────┘
                         ▼
                 ┌───────────────┐
                 │ Text Cleaning │
                 └───────┬───────┘
                         ▼
                 ┌─────────────────┐
                 │Section Detection│
                 └───────┬─────────┘
                         ▼
                 ┌───────────────┐
                 │    Chunking   │
                 └───────┬───────┘
                         ▼
                 ┌───────────────┐
                 │  Embeddings   │
                 └───────┬───────┘
                         ▼
                 ┌───────────────┐
                 │Vector Database│
                 └───────────────┘
```

---

# 🔄 Question Answering Pipeline

```text
                   User Question
                         │
                         ▼
                  Query Embedding
                         │
                         ▼
                   Vector Search
                         │
                         ▼
                    Top-K Chunks
                         │
                         ▼
                   Context Builder
                         │
                         ▼
                         LLM
                         │
                         ▼
                  Generated Answer
                         │
                         ▼
                   Source Citations
```

---

# 🛠️ Technology Stack

## Frontend

- React
- TypeScript
- Tailwind CSS

## Backend

- Python
- FastAPI
- Pydantic

## AI / ML

- PyTorch
- Hugging Face Transformers
- Sentence Transformers
- Natural Language Processing
- Transformer-based embeddings
- Large Language Models
- Retrieval-Augmented Generation

## Database

- PostgreSQL
- pgvector

## Document Processing

- PyMuPDF
- OCR support planned

## Development & Deployment

- Git
- GitHub
- Docker
- Docker Compose

---

# 📡 API Design

## Documents

```http
POST /documents/upload
GET /documents
GET /documents/{document_id}
DELETE /documents/{document_id}
```

## Search

```http
POST /search
```

## Chat

```http
POST /chat
GET /conversations
GET /conversations/{conversation_id}
```

## Paper Analysis

```http
POST /papers/{document_id}/summary
POST /papers/compare
POST /papers/research-gaps
```

## Evaluation

```http
POST /evaluation/run
GET /evaluation/results
```

---

# 🧪 Evaluation Framework

The project will evaluate the AI system using measurable metrics instead of relying only on subjective testing.

## Retrieval Metrics

- Precision@K
- Recall@K
- Mean Reciprocal Rank (MRR)
- Hit Rate

## RAG Evaluation

- Faithfulness
- Answer relevance
- Context relevance
- Citation accuracy

---

# 🔬 Experimental Evaluation

The project will support experiments comparing different configurations.

## Chunking Strategies

```text
Fixed-Size Chunking
        VS
Overlapping Chunking
        VS
Section-Aware Chunking
```

## Retrieval Size

```text
Top-K = 3
Top-K = 5
Top-K = 10
```

## Embedding Models

Different embedding models can be compared based on:

- Retrieval quality
- Semantic relevance
- Latency
- Resource requirements

All experimental results will be generated from actual experiments.

**No fabricated performance numbers will be used.**

---

# 📋 Example Questions

### General Understanding

```text
What is the main objective of this paper?
```

### Methodology

```text
Explain the methodology used in this research.
```

### Dataset

```text
Which dataset was used?
```

### Model

```text
Which machine learning model was used?
```

### Results

```text
What performance did the proposed method achieve?
```

### Limitations

```text
What limitations did the authors mention?
```

### Comparison

```text
Compare the methodologies used in these three papers.
```

### Research Gap

```text
What potential research gaps can be identified from these papers?
```

---

# 🔐 Security

The application will follow basic security practices:

- Validate uploaded files
- Restrict allowed file types
- Limit file sizes
- Sanitize filenames
- Validate API inputs
- Keep API keys in environment variables
- Never commit secrets
- Handle invalid PDFs safely
- Handle external API failures
- Use `.env.example`
- Keep `.env` excluded from Git

---

# ⚙️ Installation

## Prerequisites

Install the following:

- Python 3.11+
- Node.js 20+
- PostgreSQL
- Git
- Docker

---

## Clone Repository

```bash
git clone https://github.com/YOUR_USERNAME/AI-Research-Assistant.git

cd AI-Research-Assistant
```

---

# 🐍 Backend Setup

Create a virtual environment:

```bash
python -m venv venv
```

### Windows

```bash
venv\Scripts\activate
```

### Linux/macOS

```bash
source venv/bin/activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

# 🌐 Frontend Setup

```bash
cd frontend
npm install
```

Start the frontend:

```bash
npm run dev
```

---

# 🔑 Environment Variables

Create a `.env` file based on `.env.example`.

Example:

```env
DATABASE_URL=postgresql://username:password@localhost:5432/research_assistant

LLM_API_KEY=your_api_key_here

EMBEDDING_MODEL=your_embedding_model

TOP_K=5

MAX_FILE_SIZE_MB=20
```

### ⚠️ Important

Never upload `.env` to GitHub.

Use `.env.example` to document the required environment variables.

---

# 🐘 PostgreSQL + pgvector

The project uses PostgreSQL with the **pgvector** extension.

Conceptual database structure:

```text
PostgreSQL
│
├── documents
├── document_chunks
├── embeddings
├── conversations
└── messages
```

The vector database enables similarity-based retrieval of research-paper content.

---

# 🐳 Docker

Start the complete development environment:

```bash
docker compose up --build
```

Stop the environment:

```bash
docker compose down
```

---

# 🧪 Testing

Run backend tests:

```bash
pytest
```

Run tests with coverage:

```bash
pytest --cov=app
```

Testing will cover:

- PDF extraction
- Text chunking
- Embedding generation
- Semantic retrieval
- API endpoints
- Citation mapping
- RAG pipeline
- Error handling

---

# 🗺️ Development Roadmap

## Phase 1 — Foundation

- [ ] Repository setup
- [ ] Backend setup
- [ ] Frontend setup
- [ ] Database setup
- [ ] Docker configuration

## Phase 2 — Document Processing

- [ ] PDF upload
- [ ] PDF validation
- [ ] Text extraction
- [ ] Text cleaning
- [ ] Section detection
- [ ] Document chunking
- [ ] Metadata extraction

## Phase 3 — Embeddings & Vector Search

- [ ] Embedding model integration
- [ ] pgvector configuration
- [ ] Embedding storage
- [ ] Semantic search
- [ ] Metadata filtering

## Phase 4 — RAG

- [ ] Query embedding
- [ ] Vector retrieval
- [ ] Context construction
- [ ] LLM integration
- [ ] Grounded generation
- [ ] Citation mapping

## Phase 5 — Research Assistant

- [ ] Research chat
- [ ] Paper summaries
- [ ] Key information extraction
- [ ] Multi-paper comparison
- [ ] Research gap analysis

## Phase 6 — Evaluation

- [ ] Evaluation dataset
- [ ] Retrieval metrics
- [ ] RAG evaluation
- [ ] Citation evaluation
- [ ] Experiment tracking
- [ ] Evaluation dashboard

## Phase 7 — Production

- [ ] Security improvements
- [ ] Automated testing
- [ ] Dockerization
- [ ] Performance optimization
- [ ] Deployment
- [ ] Documentation

---

# 🚀 Future Improvements

Potential future improvements include:

- OCR for scanned research papers
- Multilingual research support
- Hybrid keyword + vector search
- Advanced reranking
- Knowledge graph integration
- Citation graph visualization
- Automatic reference extraction
- Research paper recommendation
- Literature trend analysis
- Cross-paper entity linking
- Local LLM support
- Advanced RAG evaluation
- AI research agents
- arXiv integration
- PubMed integration
- Voice-based research assistant

---

# ⚠️ Limitations

The AI Research Assistant is designed to support researchers and should not replace human verification.

Potential limitations include:

- PDF extraction errors
- Poorly formatted papers
- OCR errors
- Mathematical equation extraction limitations
- Incomplete retrieval
- LLM hallucinations
- Incorrect interpretation of ambiguous content
- Missing information in research papers

Important research claims should always be verified against the original research paper.

---

# 📸 Screenshots

Screenshots will be added after the UI implementation.

Planned interface:

```text
Dashboard
    │
    ├── Paper Library
    ├── Upload Papers
    ├── Research Chat
    ├── Semantic Search
    ├── Paper Comparison
    ├── Research Analysis
    └── Evaluation Dashboard
```

---

# 🎓 Learning Objectives

This project provides practical experience in:

## Artificial Intelligence

- Natural Language Processing
- Transformer architectures
- Embeddings
- Semantic search
- Information retrieval
- Large Language Models

## Machine Learning

- Vector representations
- Similarity search
- Ranking
- Retrieval evaluation
- Model experimentation
- Performance evaluation

## Generative AI

- LLMs
- RAG
- Prompt engineering
- Context retrieval
- Grounded generation
- LLM evaluation

## Software Engineering

- REST APIs
- Backend architecture
- Database design
- Frontend development
- Testing
- Docker
- Git/GitHub

## Research

- Experimental design
- Evaluation methodology
- Model comparison
- Retrieval evaluation
- Literature analysis
- Research gap identification

---

# 📌 Project Goals

The primary goals of this project are:

1. Make research-paper analysis faster.
2. Provide semantic search across academic papers.
3. Generate context-aware answers using RAG.
4. Provide traceable citations.
5. Support comparison of multiple research papers.
6. Extract useful research information automatically.
7. Identify potential research gaps.
8. Evaluate the AI system using measurable metrics.
9. Demonstrate practical AI/ML engineering skills.
10. Build a production-quality portfolio project.

---

# 👨‍💻 Author

## Shaikh Mohammed Sohail

**B.Tech Computer Science Engineering — Artificial Intelligence & Machine Learning**

### Areas of Interest

- Artificial Intelligence
- Machine Learning
- Generative AI
- Natural Language Processing
- Deep Learning
- Data Analytics
- Software Development

---

# 📄 License

This project is licensed under the **MIT License**.

See the `LICENSE` file for details.

---

# ⭐ Support

If you find this project useful or interesting, consider giving the repository a ⭐.

---

## 🚧 Project Status

**Under Development**

The project is being developed incrementally with a focus on:

- Practical AI/ML implementation
- Explainable retrieval
- Citation-grounded generation
- Scientific evaluation
- Clean software architecture
- Production-ready development practices
```

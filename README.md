# PDF AI Assistant (RAG)

A Streamlit-powered web app that lets you chat with multiple PDF documents. Built using **Retrieval-Augmented Generation (RAG)** to provide accurate, hallucination-free answers with exact source citations.

## Key Features
- **Multi-PDF Support:** Upload and analyze multiple documents simultaneously.
- **Semantic Search:** Understands query intent using vector embeddings, not just keywords.
- **Source Citations:** Every answer includes exact references (File Name & Page Number).
- **Optimized RAG:** Smart text chunking and local vector storage for fast retrieval.

## Tech Stack
- **Frontend:** Streamlit
- **AI & Embeddings:** OpenAI API (`gpt-4o-mini`, `text-embedding-3-small`)
- **Vector DB:** ChromaDB
- **Processing:** LangChain, PyPDF

## ️ How It Works
1. **Ingest & Embed:** PDFs are split into chunks and converted to vectors.
2. **Retrieve:** User queries fetch the top 5 most relevant chunks from ChromaDB.
3. **Generate:** GPT-4o-mini generates an answer using *only* the retrieved context.

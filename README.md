# Using FAISS as a Vector Database for Question Answering from PDFs

This project enables **intelligent question-answering** on ESG (Environmental, Social, and Governance) or sustainability reports in **PDF format** using **semantic search** and **transformer-based NLP models**.  

It converts PDF text into **semantic embeddings**, stores them in a **FAISS vector index**, and uses **Transformer models** to retrieve and answer natural language questions accurately.

## Overview

Traditional keyword searches are limited — they fail when users ask questions naturally such as:

> “What sustainability initiatives did Amazon report in 2020?”

This project leverages **vector database**, **semantic search** and **transformers and embeddings** to understand the meaning of the question and find the most relevant sections across PDF reports.

## Concept

A Vector Database (Vector DB) is a database designed to store and search data represented as vectors. A Vector DB is mainly used for understanding the context of keywords/sentences, using similarity search. It compares embeddings of any query against embeddings of stored text, and the most similar vectors are retrieved.
FAISS:  FAISS is an open-source library by Facebook AI. Optimized for fast nearest neighbour search across millions of vectors and runs entirely locally (no cloud dependency).
Some of the Strengths of FAISS are:
o	Simple to set up (no external service required).
o	Very fast at similarity search (GPU support available).
o	Works well for small-to-medium scale projects.

1. **PDF Extraction**: Text Mining - Extract text from ESG PDF reports
2. **Chunking**: Text Preprocessing - Split long text into smaller overlapping segments
3. **Embedding Generation**: Sentence Transformers - Convert text into numerical (semantic) vectors
4. **Vector Indexing**: FAISS - Efficiently store and retrieve similar text embeddings
5. **Semantic Search**: Similarity Search - Retrieve text chunks closest to the question vector
6. **QA / Summarization**: NLP Transformers - Use pretrained models to extract or summarize answers

## How the Code Works

The main objective of the Use-Case is to understand how to build a semantic search engine for PDF files using a Vector DB. FAISS works best when extracting answers from a collection of ESG Reports of various companies across different years as it provides a local, lightweight, fast similarity search. Other DBs like Chroma, Weaviate, Pinecone are great for large-scale apps or production APIs, but FAISS is perfect for prototyping and personal analysis. FAISS ensures results are fast and precise, even across thousands of chunks.
The combination of: Sentence embeddings (semantic meaning) and Vector database (FAISS) (efficient similarity search) makes the model robust for answers to be provided for any kind of long, large sized reports. 

1. Extract text from all ESG report PDFs.  
2. Split the text into overlapping chunks for better context.  
3. Encode chunks into dense vectors using a **SentenceTransformer** model.  
4. Build a **FAISS vector index** to enable fast semantic search.  
5. When a question is asked, it’s converted into a vector.  
6. The most semantically similar chunks are retrieved.  
7. The answer is generated using a **Question Answering** or **Summarization** model.

## Conclusion 

The project demonstrates how to build a semantic search engine for PDFs using FAISS.
•	Vector DB concept: store embeddings for semantic similarity.
•	FAISS: chosen for simplicity, speed, and local setup.
•	Code flow: PDF → text chunks → embeddings → FAISS index → query embedding → semantic search results.
This approach ensures the extraction of accurate, precise, and complete answers from large, unstructured PDF documents like ESG/Sustainability reports.



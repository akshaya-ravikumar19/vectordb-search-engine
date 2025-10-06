# ESG Report Question-Answering using PDFs, FAISS & Transformers

This project enables **intelligent question-answering** on ESG (Environmental, Social, and Governance) or sustainability reports in **PDF format** using **semantic search** and **transformer-based NLP models**.  

It converts PDF text into **semantic embeddings**, stores them in a **FAISS vector index**, and uses **Transformer models** to retrieve and answer natural language questions accurately.

## Overview

Traditional keyword searches (like Ctrl + F) are limited — they fail when users ask questions naturally such as:

> “What sustainability initiatives did Amazon report in 2020?”

This project leverages **semantic search** and **transformers** to understand the meaning of the question and find the most relevant sections across PDF reports.


## Concept

1. **PDF Extraction**:Text Mining - Extract text from ESG PDF reports
2. **Chunking**:Text Preprocessing - Split long text into smaller overlapping segments
3. **Embedding Generation**:Sentence Transformers - Convert text into numerical (semantic) vectors
4. **Vector Indexing**:FAISS - Efficiently store and retrieve similar text embeddings
5. **Semantic Search**:Similarity Search - Retrieve text chunks closest to the question vector
6. **QA / Summarization**:NLP Transformers - Use pretrained models to extract or summarize answers

## How the Code Works

1. Extract text from all ESG report PDFs.  
2. Split the text into overlapping chunks for better context.  
3. Encode chunks into dense vectors using a **SentenceTransformer** model.  
4. Build a **FAISS vector index** to enable fast semantic search.  
5. When a question is asked, it’s converted into a vector.  
6. The most semantically similar chunks are retrieved.  
7. The answer is generated using a **Question Answering** or **Summarization** model.


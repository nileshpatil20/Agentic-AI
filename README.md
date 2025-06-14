# Agentic-AI

## Overview
This repository demonstrates agentic AI workflows using LangChain and LangGraph. It includes scripts and notebooks for building, embedding, storing, and retrieving data with vector databases, as well as orchestrating agentic reasoning and decision-making.

## Agentic Workflow Steps

### 1. Data Ingestion & Preparation
- Load data from various sources (text, PDF, web, etc.).
- Use loaders like `TextLoader`, `DirectoryLoader`, or `PyPDFLoader` from LangChain.
- Split documents into manageable chunks using `RecursiveCharacterTextSplitter`.

### 2. Embedding Generation
- Select an embedding model (e.g., HuggingFace, OpenAI, Google Generative AI).
- Generate vector representations for each document chunk using the embedding model.

### 3. Vector Database Storage
- Choose a vector database (e.g., FAISS, Chroma, Pinecone).
- Store the embeddings and associated metadata in the vector database for efficient similarity search.

### 4. Retrieval
- Use a retriever to find relevant documents based on user queries.
- Retrieve top-k most similar chunks using vector similarity (cosine, L2, etc.).

### 5. Agentic Reasoning with LangGraph
- Define agent state and workflow using LangGraph's `StateGraph`.
- Create nodes for classification, retrieval-augmented generation (RAG), and LLM-based answering.
- Route queries through the workflow based on their content (e.g., classify, retrieve, or answer directly).
- Use conditional edges to control the flow between nodes.

### 6. Output Generation
- Use prompt templates and output parsers to format and present answers.
- Chain together retrieval and LLM calls for context-aware, agentic responses.

## Example Workflow
1. **User Query** → 2. **Classification Node** (LangGraph) → 3. **RAG Node** (if needed) → 4. **LLM Node** → 5. **Final Answer**

## Requirements
- Python 3.8+
- See `requirements.txt` for all dependencies

## Getting Started
1. Clone the repository
2. Set up a virtual environment and install requirements
3. Add your `.env` file with necessary API keys
4. Run the notebooks or scripts as needed

---

Feel free to explore the code and adapt the workflow for your own agentic AI projects!

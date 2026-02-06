# RAG Project

This project implements a RAG (Retrieval-Augmented Generation) system using LangChain, OpenAI, and ChromaDB to answer questions based on PDF documents. The goal is to demonstrate how to create an application capable of "reading" documents and answering questions about them using Artificial Intelligence.

## 🛠️ Stack Used

<img src="https://skillicons.dev/icons?i=python,vscode,git" alt="python,vscode,git" />

### Other tools:

- [Ruff](https://docs.astral.sh/ruff/)
- [uv](https://docs.astral.sh/uv/)
- [Antigravity](https://antigravity.google/)
- [OpenAI](https://openai.com/)
- [ChromaDB](https://www.trychroma.com/)
- [LangChain](https://www.langchain.com/)

## 📋 Prerequisites

Before you begin, you will need:

- Python 3.12 or higher installed.
- An OpenAI account and an [API key](https://platform.openai.com/api-keys).
- The [`uv`](https://github.com/astral-sh/uv) package manager (optional, but recommended for speed) or `pip`.

## ⚙️ Installation and Setup

1. **Install dependencies**:

   This project uses `pyproject.toml` for dependency management.

   If using **uv** (recommended):

   ```bash
   uv sync
   ```

   Or using traditional **pip**:

   ```bash
   pip install -e .
   ```

2. **Configure environment variables**:

   The project requires your OpenAI API key to work.

   Rename the example file:

   ```bash
   cp .env.example .env
   ```

   Open the `.env` file and insert your key:

   ```env
   OPENAI_API_KEY=sk-...
   ```

## 📖 How to Use

1. **Add your Documents**:
   Place the PDF files you want to process inside the `documents/` folder.

   > _The current code is configured to read a specific file (e.g., `documents/DOC-MPV-13082025-20250808.pdf`). You can change the file path in the notebook._

2. **Run the RAG**:
   Open the `rag_solution.ipynb` notebook in VS Code or Jupyter Notebook.

   Run the cells sequentially to:
   - Load and process the PDF.
   - Create and persist embeddings in ChromaDB (`chroma_db/` folder).
   - Initialize the chat model.
   - Ask questions about the document.

# MongoDB RAG (Retrieval-Augmented Generation)

![RAG With MongoDB architecture](media/implementation_architecture.png)
**RAG With MongoDB architecture**

## Overview
This project demonstrates a full Retrieval-Augmented Generation (RAG) pipeline using MongoDB as a vector database and OpenAI-compatible models (e.g., via LM Studio) for embeddings and generation. The workflow covers data ingestion, vector search, and answer generation.




## Features
- **Modern Python project setup** using [uv](https://github.com/astral-sh/uv) for fast, reproducible dependency management.
- **PDF ingestion and chunking** using `langchain` and `pypdf` for efficient document processing.
- **Embeddings** generated with OpenAI-compatible models (tested with LM Studio, can be replaced with other providers).
- **MongoDB Atlas** for storing and searching vector embeddings, enabling scalable and secure data storage.
- **Vector search and retrieval** using MongoDB's vector index for high-performance similarity search.
- **LLM-based answer generation** from retrieved context, supporting advanced question answering.
- **Jupyter Notebook workflow** for step-by-step experimentation and reproducibility.
- **Extensible design**: Easily adapt to other embedding models, document types, or databases.

## Project Structure
- `main.py`: Entry point (demo/placeholder).
- `mongo_db_connection.py`: MongoDB connection logic and test connection.
- `rag.ipynb`: Jupyter notebook with the full RAG workflow (data ingestion, retrieval, generation).
- `requirements.txt` / `pyproject.toml`: Project dependencies and metadata.


## Setup Instructions
1. **Clone the repository**
2. **Install dependencies** (recommended: use `uv`):
  ```sh
  uv pip install -r requirements.txt
  ```
  Or use pip:
  ```sh
  pip install -r requirements.txt
  ```
3. **Configure MongoDB**: Update your MongoDB credentials in notebook if needed.
4. **Run the notebook**: Open `rag.ipynb` in Jupyter and follow the cells for data ingestion, retrieval, and generation.
5. **(Optional) Run scripts**: Use `main.py` or extend the code for CLI or API usage.


## Example Workflow
1. **Ingest PDF**: Load and split a PDF, generate embeddings, and store them in MongoDB.
2. **Create Vector Index**: Set up a vector index in MongoDB for similarity search.
3. **Query**: Embed a query, retrieve the most relevant document chunks from MongoDB.
4. **Generate Answer**: Use an LLM to generate an answer from the retrieved context.
5. **Iterate and Experiment**: Modify prompts, try different models, or use your own data for further experimentation.


---

## Best Practices & Tips
- Use environment variables or secrets management for sensitive credentials.
- For large-scale or production use, consider batching, error handling, and logging.
- You can swap out the embedding or LLM provider by changing the relevant code sections.
- The notebook is designed for experimentation—adapt it for scripts or APIs as needed.

![Example showing how to setup models in LM Studio for both Embedding and Generation.](media/LM_studio_setup.png)
**Example showing how to setup models in LM Studio for both Embedding and Generation.**



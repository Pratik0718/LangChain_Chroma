# # IPL Player Vector Store with LangChain & Chroma DB

This project demonstrates how to build and manage a local, open-source Vector Database using **LangChain** and **Chroma DB** to store, search, and manage structured information about IPL players.

Unlike traditional setups that rely on external APIs like OpenAI, this notebook uses a completely free, open-source embedding model running locally.

## 🚀 Features Demonstrated
- **Open-source Embeddings**: Utilizes the `all-MiniLM-L6-v2` Hugging Face transformer model to convert texts into vector embeddings locally.
- **Document Storage**: Organizes textual player details as LangChain `Document` objects with integrated metadata (e.g., team names).
- **Similarity Search**: Performs semantic queries over stored player documents (e.g., finding bowlers).
- **Metadata Filtering**: Filters search results targeting specific metadata values (e.g., searching specifically for `Chennai Super Kings` players).
- **CRUD Operations on Vector Database**:
  - **Create**: Adding documents via `vector_store.add_documents`.
  - **Read**: Retrieving stored items, metadata, and embeddings with `vector_store.get()`.
  - **Update**: Modifying existing stored vector items using their unique IDs.
  - **Delete**: Removing items from the vector collection using IDs.

## 🛠️ Prerequisites & Installation
To run this code, install the required packages:
```bash
pip install langchain chromadb sentence-transformers langchain-community
```

## 📖 How to Use
1. **Define Documents**: Create LangChain `Document` objects containing your text data and metadata.
2. **Initialize Embeddings & DB**: Load `HuggingFaceEmbeddings` and connect them to a local `Chroma` instance specifying a local persistence directory.
3. **Query & Manipulate**: Run similarity searches or perform document metadata updates directly using the initialized vector store instance.

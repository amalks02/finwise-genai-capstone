# Embedding + Retrieval with FAISS

This project enables Question Answering (Q&A) over documents (loan brochures, KYC policies, compliance manuals, etc.) using embeddings and FAISS as the vector database.

How It Works
## 1. Embeddings

 - Each text chunk from the document is converted into a high-dimensional vector (embedding).

 - Embeddings capture semantic meaning → sentences with similar meaning will have embeddings that are close in vector space.

 - Example:

   "Eligibility criteria for home loan" → [0.23, -0.87, 0.14, ...]

   "Who can apply for a home loan?" → [0.21, -0.84, 0.15, ...]
    These vectors are very close to each other.

### Supported Embedding Models:

  - google-vertexai-embedding-001 (Google Vertex AI)

  - text-embedding-ada-002 (OpenAI)

  - all-MiniLM-L6-v2 (Sentence Transformers)

## 2. Vector Store (FAISS)

 - FAISS = Facebook AI Similarity Search (a library for fast nearest-neighbor search).

 - Stores all embeddings in a highly optimized index for similarity search.

 - Allows quick retrieval of the most relevant chunks given a query.

### Indexing Process:

   - Split PDF into text chunks.

   - Embed each chunk into a vector.

   - Store vectors in FAISS index.

## 3. Retrieval

  - When a user asks a question, that query is embedded into the same vector space.

  - FAISS searches for the k most similar embeddings (nearest neighbors).

  - The matching chunks are returned as the context.

## 4. Answer Generation

  - Retrieved chunks are passed to the LLM (Gemini / GPT) as context.

  - The LLM generates a natural language answer, constrained to the retrieved information.

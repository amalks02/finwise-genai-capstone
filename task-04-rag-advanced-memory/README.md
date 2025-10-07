## Banking chat bot with advanced memory
This project demonstrates how to extend a Question-Answering (QA) system with memory and multi-turn dialogue using LangChain, Gemini Pro, and FAISS.
It enables the AI to remember previous user interactions and compare or relate new questions to earlier ones — creating a more human-like, context-aware conversation experience.

### Objective
Build a multi-step retrieval QA system that:
- Understands context from previous turns in a conversation.
- Reformulates user questions automatically using multi-query retrieval.
- Recalls and compares previous responses for deeper insights.

### Code Workflow
1. Extract Text from PDF
  - Reads and concatenates all pages using pypdf.PdfReader.

2. Split into Chunks
  - Splits long text into overlapping word chunks (default: 500 words, 50 overlap).
3. Create FAISS Vector Store
  - Embeds text using all-MiniLM-L6-v2 and stores embeddings in FAISS for fast retrieval.
4. Initialize Gemini Pro LLM
  - Sets up the ChatGoogleGenerativeAI model with temperature control.
5. Add Multi-Query Retrieval
  - Enhances search accuracy by reformulating queries internally.
6. Enable Memory
  - Stores chat history for multi-turn conversation handling.
7. Build Conversational Chain
  - Combines retriever, LLM, and memory into a single workflow.
8. Run Interactive QA
  - Start a terminal session and query your document interactively.

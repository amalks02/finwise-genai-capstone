# Banking Chatbot with Memory

This project is a simple banking assistant chatbot built using Google Gemini (via LangChain) and Gradio.
It demonstrates how to combine LLMs, memory, and rule-based logic to answer customer queries with context.

### Features

- Gemini Pro LLM integration via LangChain.

- Conversation memory 

- Rule-based responses for banking actions (Balance inquiry,Credit card payment/transfer)

- Fallback to LLM for open-ended questions.

- Interactive Gradio interface for chatting.


### Tech Stack

- Google Generative AI 

- LangChain 

- Memory: ConversationBufferMemory 

- Gradio for chatbot UI

### Logic Flow

- LLM Setup

  - Gemini Pro (ChatGoogleGenerativeAI) is used as the chatbot engine.

  - Memory Initialization

  - ConversationBufferMemory(return_messages=True) keeps track of conversation history.

  - Preloads dummy customer data (name, balance, credit card due) into memory.

- User Query Processing

  - If the query is about balance, return balance from customer_data.

  - If the query is a transfer request, deduct balance and update credit card dues.

  - Otherwise, pass the query to Gemini Pro via ConversationChain.

- UI Layer

  - Built with Gradio (gr.Blocks, gr.Chatbot, gr.Textbox).

  - Users type questions → chatbot responds → history is displayed.

### Memory Type Used

- ConversationBufferMemory

  - Stores the entire dialogue history in a buffer.

  - Keeps track of both user and AI messages.

  - Ensures the LLM has context from previous turns.

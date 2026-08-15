# InsureLLM - RAG - ChatBot
A Retrieval-Augmented Generation (RAG) chatbot that answers questions about Insurellm, an insurance-tech company, using its internal knowledge base (employee records, contracts, etc.). The bot retrieves relevant context from a vector database and uses a large language model to generate grounded, conversational answers through a simple web chat UI.
## Features
- 🔎 Semantic retrieval over a local knowledge base using Chroma as the vector store
- 🧠 Sentence-transformer embeddings (all-MiniLM-L6-v2 via HuggingFace) for fast, local embedding generation
- 💬 LLM-powered answers using Google's Gemini (gemini-2.5-flash) through LangChain
- 🖥️ Interactive chat UI built with Gradio
- 🗂️ Context-aware responses grounded in retrieved documents (employees, contracts, and more)
## Tech Stack
LLM	Google Gemini (gemini-2.5-flash) via langchain_google_genai<br>
Embeddings	HuggingFace all-MiniLM-L6-v2<br>
Vector Store	Chroma (langchain_chroma)<br>
Orchestration	LangChain<br>
UI	Gradio ChatInterface<br>
Environment	Python 3.13, python-dotenv<br>
## How it Works
- A knowledge base of documents (e.g. employee profiles, contracts) is embedded using a HuggingFace sentence-transformer model and stored in a persistent Chroma vector database.
- When a user asks a question, the retriever fetches the most relevant document chunks from the vector store.
- The retrieved context is injected into a system prompt, which is sent along with the user's question to the Gemini LLM.
- The LLM generates a response grounded in the retrieved context, and the answer is displayed in a Gradio chat interface.
## Vector Database
Make sure a Chroma vector store (vector.db) has been created and populated with your knowledge base documents before running the app. The knowledge base used in this project includes files such as employee records and contracts under a knowledge-base/ directory.

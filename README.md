# InsureLLM - RAG - ChatBot
A Retrieval-Augmented Generation (RAG) chatbot that answers questions about Insurellm, an insurance-tech company, using its internal knowledge base (employee records, contracts, etc.). The bot retrieves relevant context from a vector database and uses a large language model to generate grounded, conversational answers through a simple web chat UI.
## Features
- 🔎 Semantic retrieval over a local knowledge base using Chroma as the vector store
- 🧠 Sentence-transformer embeddings (all-MiniLM-L6-v2 via HuggingFace) for fast, local embedding generation
- 💬 LLM-powered answers using Google's Gemini (gemini-2.5-flash) through LangChain
- 🖥️ Interactive chat UI built with Gradio
- 🗂️ Context-aware responses grounded in retrieved documents (employees, contracts, and more)

🚀 Overview
This repository features a powerful Retrieval-Augmented Generation (RAG) application built with Streamlit, leveraging Groq's lightning-fast Llama3-8b-8192 LLM, and Ollama Embeddings. This tool allows you to interactively query your PDF research papers and get accurate answers based only on the provided document context.

Say goodbye to information overload! With this RAG application, you can quickly extract precise information from your documents, making research and data analysis incredibly efficient.

✨ Features
Intelligent Q&A: Ask natural language questions about your PDF documents.
Context-Aware Responses: Answers are strictly generated from the provided document content, minimizing hallucinations.
🚀 Blazing Fast Inferences: Powered by Groq's optimized Llama3 model, providing near-instantaneous responses.
Local Embeddings: Utilizes Ollama for local embedding generation, ensuring data privacy and offline capability.
Streamlit UI: A clean, intuitive, and interactive web interface for a seamless user experience.
Scalable: Easily adaptable to different research papers or document sets.
🛠️ Technologies Used
Streamlit: For building the interactive web application.
LangChain: For orchestrating the RAG pipeline (document loading, text splitting, vector store, retrieval, and chain creation).
Groq: For incredibly fast LLM inference with the Llama3-8b-8192 model.
Ollama: For generating local document embeddings.
FAISS: For efficient similarity search and vector storage.
PyPDFDirectoryLoader: For loading PDF documents.
python-dotenv: For managing environment variables (API keys).
⚡ Quick Start
Follow these steps to get your RAG application up and running in no time!

Prerequisites
Before you begin, ensure you have the following installed:

Python 3.8+
Ollama: Download and install Ollama from https://ollama.com/ and pull the llama3 model by running ollama pull llama3 in your terminal.
Groq API Key: Obtain a free API key from https://console.groq.com/keys.

🚀 How to Use
Upload Documents: Ensure your PDF research papers are in the research_papers directory.
Click "Document Embedding": This button processes your PDFs, splits them into chunks, generates embeddings using Ollama, and creates a FAISS vector database. You'll see "Vector Database is ready" once this is complete. This step only needs to be done once per session or if you add new documents.
Enter Your Query: Type your question related to the research papers in the text input box.
Get Your Answer: The application will then retrieve relevant document snippets and use Groq's Llama3 to generate a precise answer based on the context.
Explore Context: Expand the "Document similarity Search" section to see the exact document chunks that were used to formulate the answer, providing transparency and traceability.

# RAG Document Q&A with Groq and Llama3

---

## 🚀 Overview

This repository features a powerful **Retrieval-Augmented Generation (RAG)** application built with **Streamlit**, leveraging **Groq's lightning-fast Llama3-8b-8192 LLM**, and **Ollama Embeddings**. This tool allows you to interactively query your PDF research papers and get accurate answers based **only** on the provided document context.

Say goodbye to information overload! With this RAG application, you can quickly extract precise information from your documents, making research and data analysis incredibly efficient.

## ✨ Features

* **Intelligent Q&A:** Ask natural language questions about your PDF documents.
* **Context-Aware Responses:** Answers are strictly generated from the provided document content, minimizing hallucinations.
* **🚀 Blazing Fast Inferences:** Powered by Groq's optimized Llama3 model, providing near-instantaneous responses.
* **Local Embeddings:** Utilizes Ollama for local embedding generation, ensuring data privacy and offline capability.
* **Streamlit UI:** A clean, intuitive, and interactive web interface for a seamless user experience.
* **Scalable:** Easily adaptable to different research papers or document sets.

## 🛠️ Technologies Used

* **Streamlit:** For building the interactive web application.
* **LangChain:** For orchestrating the RAG pipeline (document loading, text splitting, vector store, retrieval, and chain creation).
* **Groq:** For incredibly fast LLM inference with the Llama3-8b-8192 model.
* **Ollama:** For generating local document embeddings.
* **FAISS:** For efficient similarity search and vector storage.
* **PyPDFDirectoryLoader:** For loading PDF documents.
* **python-dotenv:** For managing environment variables (API keys).

## ⚡ Quick Start

Follow these steps to get your RAG application up and running in no time!

### Prerequisites

Before you begin, ensure you have the following installed:

* **Python 3.8+**
* **Ollama:** Download and install Ollama from [https://ollama.com/](https://ollama.com/) and pull the `llama3` model by running `ollama pull llama3` in your terminal.
* **Groq API Key:** Obtain a free API key from [https://console.groq.com/keys](https://console.groq.com/keys).

### Installation

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/your-username/rag-groq-streamlit.git](https://github.com/your-username/rag-groq-streamlit.git)
    cd rag-groq-streamlit
    ```

2.  **Create a virtual environment (recommended):**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3.  **Install the required dependencies:**
    ```bash
    pip install -r requirements.txt
    ```
    *(Note: You'll need to create a `requirements.txt` file based on the provided code. A basic one would include: `streamlit`, `langchain`, `langchain-groq`, `langchain-community`, `pypdf`, `python-dotenv`)*

4.  **Set up your environment variables:**
    Create a `.env` file in the root directory of your project and add your Groq API key:
    ```
    GROQ_API_KEY="your_groq_api_key_here"
    ```
    Replace `"your_groq_api_key_here"` with the actual API key you obtained from Groq.

5.  **Place your research papers:**
    Create a directory named `research_papers` in the root of your project and place your PDF documents inside it. The application will load all PDFs from this directory.

### Running the Application

1.  **Start the Streamlit application:**
    ```bash
    streamlit run app.py
    ```
    *(Assuming your main Streamlit script is named `app.py`)*

2.  **Access the application:**
    Your web browser will automatically open to the Streamlit application (usually at `http://localhost:8501`).

## 🚀 How to Use

1.  **Upload Documents:** Ensure your PDF research papers are in the `research_papers` directory.
2.  **Click "Document Embedding":** This button processes your PDFs, splits them into chunks, generates embeddings using Ollama, and creates a FAISS vector database. You'll see "Vector Database is ready" once this is complete. This step only needs to be done once per session or if you add new documents.
3.  **Enter Your Query:** Type your question related to the research papers in the text input box.
4.  **Get Your Answer:** The application will then retrieve relevant document snippets and use Groq's Llama3 to generate a precise answer based on the context.
5.  **Explore Context:** Expand the "Document similarity Search" section to see the exact document chunks that were used to formulate the answer, providing transparency and traceability.

## 📂 Project Structure

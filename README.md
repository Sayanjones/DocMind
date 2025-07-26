# DocMind: Document-Based Q&A Retrieval System


This repository contains the implementation of a **Document Q&A Application** that utilizes **LangChain**, **FAISS**, and **Google Generative AI Embeddings** for vector-based similarity search and document-based question answering.

## Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Prerequisites](#prerequisites)
- [Setup and Installation](#setup-and-installation)
- [How to Run the Application](#how-to-run-the-application)
- [Project Workflow](#project-workflow)
- [Dependencies](#dependencies)
- [License](#license)

---

## Introduction
The **Gemma Model Document Q&A Application** is a Streamlit-based tool that uses advanced language models like **Groq Llama3-8b-8192** and **Google Generative AI Embeddings** to answer user queries based on the contents of uploaded documents.  
It enables:
1. **PDF ingestion and processing.**  
2. **Chunked document embeddings for efficient retrieval.**  
3. **Question-answering based on context-relevant documents.**

---

## Features
- **Streamlit UI:** Interactive web interface for document embedding and querying.
- **FAISS Vector Store:** Efficient vector-based similarity search.
- **LangChain Integration:** Structured document chains and retrieval chains.
- **Google Generative AI Embeddings:** High-quality embedding generation for context retrieval.
- **PDF Document Processing:** Support for loading multiple PDF documents.

---

## Prerequisites
- Python 3.8 or higher
- API keys for:
  - **Groq API** (`GROQ_API_KEY`)
  - **Google API** (`GOOGLE_API_KEY`)

---

## Setup and Installation
1. **Clone the Repository:**
   ```bash
   git clone https://github.com/your-username/gemma-document-qa.git
   cd gemma-document-qa
   ```

2. **Create a Virtual Environment:**
   ```bash
   python -m venv env
   source env/bin/activate  # On Windows: env\Scripts\activate
   ```

3. **Install Dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Environment Configuration:**
   Create a `.env` file in the root directory and add:
   ```plaintext
   GROQ_API_KEY=<your_groq_api_key>
   GOOGLE_API_KEY=<your_google_api_key>
   ```

5. **Data Setup:**
   - Place the PDF documents you want to process in the `us_census` directory.

---

## How to Run the Application
1. **Start the Streamlit App:**
   ```bash
   streamlit run app.py
   ```

2. **Steps to Use:**
   - **Step 1:** Click on the "Documents Embedding" button to load and process the documents.
   - **Step 2:** Enter your question in the input field.
   - **Step 3:** View the AI-generated answer and related document excerpts.

---

## Project Workflow
1. **Data Ingestion:** Load PDF documents using `PyPDFDirectoryLoader`.
2. **Text Splitting:** Chunk documents into smaller pieces using `RecursiveCharacterTextSplitter`.
3. **Vector Store Creation:** Use FAISS for embedding and similarity search.
4. **Prompt Engineering:** Define a structured prompt for the language model.
5. **Query Processing:**
   - Use the retrieval chain to fetch relevant chunks.
   - Generate answers based on the query and relevant context.

---

## Dependencies
The project relies on the following libraries and frameworks:
- **Streamlit:** Web application framework.
- **FAISS (faiss-cpu):** Vector search library for similarity search.
- **LangChain:** Framework for creating structured chains.
- **PyPDF2:** Library for handling PDF documents.
- **Google Generative AI Embeddings:** Pre-trained embeddings for document representation.
- **python-dotenv:** Manage environment variables.

Install dependencies via `requirements.txt`:
```plaintext
streamlit
faiss-cpu
langchain
langchain_google_genai
langchain_community
PyPDF2
python-dotenv
```

---

## License
This project is licensed under the [MIT License](LICENSE).  

Feel free to contribute and make this project better! 😊  

--- 

Happy coding! 🌟

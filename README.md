# Conversational RAG with PDF Uploads and Chat History
This repository contains a Streamlit-based application that allows users to upload PDF documents and interact with their content through a conversational interface. The application integrates LangChain for retrieval-augmented generation (RAG) and provides chat history support for context-aware responses using Groq's LLM API.

## Features
- PDF Uploads: Users can upload multiple PDF files and extract their content for further interactions.
- Retrieval-Augmented Generation (RAG): Combines document retrieval with language model capabilities to answer user questions based on the uploaded content.
- Stateful Chat Interface: Maintains chat history for more accurate responses, especially when questions refer to earlier parts of the conversation.
- Vector Store with FAISS: Leverages FAISS (instead of Chroma) for fast and efficient document retrieval by creating embeddings from the uploaded PDFs.
- Contextualized Questions: Reformulates user questions based on the chat history to make them understandable even without previous context.
## Requirements:
- Streamlit: Frontend for uploading files and interacting with the assistant.
- LangChain: Manages document retrieval, chat history, and communication with the LLM.
- Groq's LLM API: Used for generating responses from the `Gemma2-9b-It model`.
- FAISS: Efficient vector search for document retrieval.
- HuggingFace Embeddings: Used to generate embeddings from PDF content.

Set up environment variables:

Create a `.env` file in the root directory of the project and add your HuggingFace and Groq API keys:

  ```bash
    HF_TOKEN=your_huggingface_token
    GROQ_API_KEY=your_groq_api_key
  ```

Run the Streamlit app:
  ```bash
    streamlit run app.py
  ```

## Usage
1. Open the app in your browser after running Streamlit.
2. Enter your Groq API key when prompted.
3. Upload one or more PDF files.
4. Type your questions related to the PDF content in the chat input.
5. View the assistant’s responses along with the chat history.


# Indian Geography Question-Answering using RAG

This project presents a Retrieval-Augmented Generation (RAG) system designed to answer questions about Indian geography. It leverages local large language models (LLMs) via Ollama, specifically the Llama3 model, integrated with the Langchain framework. The system gathers information from Wikipedia, processes it, and uses it as context to generate accurate and relevant answers.

---

## **Project Overview**

This project allows users to ask questions about **Indian Geography**, and the system responds using context retrieved from a vector store. Instead of relying purely on the LLM, the system enhances accuracy by grounding responses in real text sources.

## How it Works (RAG Pipeline)

1.  **Data Collection**: Wikipedia articles related to specific Indian geographical terms (e.g., states, cities, general geography) are fetched.
2.  **Document Chunking**: The lengthy articles are broken down into smaller, manageable pieces to facilitate efficient retrieval.
3.  **Embedding & Storage**: Each text chunk is converted into a numerical vector (embedding) using Ollama's Llama3 embedding model. These embeddings, along with their original text, are stored in a Chroma vector database.
4.  **Retrieval**: When a question is posed, the system identifies and retrieves the most semantically similar text chunks from the Chroma database.
5.  **Generation**: The retrieved context and the user's question are then fed to the Llama3 LLM (running via Ollama) to synthesize a comprehensive and contextually accurate answer.

## **Features**

* Retrieval-Augmented Generation (RAG) pipeline
* Embedding-based similarity search
* Vector store implementation
* Question answering over Indian Geography
* Modular, easy-to-extend notebook
* Supports any text corpus

---

## Technologies Used

*   **Langchain**: For orchestrating the RAG pipeline.
*   **Ollama**: To host and run the Llama3 LLM locally.
*   **Llama3**: The chosen Large Language Model for embeddings and text generation.
*   **Wikipedia API**: For data ingestion.
*   **Chroma**: A lightweight, in-memory vector store.

---

## Example Output

```
User Question: "Tell me about Gujarat State"

RAG Answer:
"Gujarat is a state located along the western coast of India, with a coastline of about 2,340 km (1,450 mi) and an area of 196,024 km2 (75,685 sq mi). It has a population of 60.4 million people as of 2011."
```
---

## **Use Cases**

* Educational question answering
* Geography learning assistant
* AI-powered study tool
* RAG pipeline demonstration

Just tell me!

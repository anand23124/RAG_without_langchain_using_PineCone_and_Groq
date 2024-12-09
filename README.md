# RAG System Using Pinecone, Groq, and Sentence Transformers

This project demonstrates how to build a Retrieval-Augmented Generation (RAG) system without using Langchain. The system uses Pinecone for vector search, Groq for model inferencing, and Sentence Transformers for embeddings.

## Requirements

- Pinecone API key
- Groq API key
- SentenceTransformers library
- Pinecone and Groq Python clients

## Steps to Run

1. Clone the repository:
    ```bash
    git clone https://github.com/anand23124/RAG_without_langchain_using_PineCone_and_Groq.git
    cd RAG_without_langchain_using_PineCone_and_Groq
    ```

2. Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```

3. Initialize Pinecone and Groq with your API keys:
    ```python
    pinecone.init(api_key="your-pinecone-api-key", environment="us-west1-gcp")
    ```

4. Process and add documents to Pinecone:
    ```python
    process_and_add_documents_to_pinecone(pinecone_index, "path_to_documents")
    ```

5. Run a RAG query:
    ```python
    query = "When was GreenGrow Innovations founded?"
    response, sources = rag_query(pinecone_index, query)
    ```

## License

This project is licensed under the MIT License.



# Langchain-Based Question Answering System

This project implements a question-answering system using Langchain’s retrieval-augmented generation (RAG) pipeline with OpenAI’s GPT-3.5-turbo model. It retrieves relevant documents, processes them, and generates concise, cost-efficient answers.

## Features

- **Document Retrieval**: Uses FAISS for fast document retrieval, ensuring relevant information is fetched from the loaded content.
- **Language Model**: Utilizes the GPT-3.5-turbo model for natural language processing, generating responses based on provided context.
- **Token Cost Tracking**: Tracks API usage cost, computing the total cost of each query based on prompt and completion tokens.
- **Document Splitting**: Documents are split into manageable chunks for efficient processing using recursive text splitting.

## Components

1. **LLM Setup**: The project sets up GPT-3.5-turbo with custom parameters for maximum token usage, temperature, top_p, and penalty settings.
2. **Document Loader**: Loads documents from a web source and splits them into chunks to store in the FAISS vector store.
3. **Embeddings**: Creates embeddings from the document chunks using OpenAI Embeddings, storing them in FAISS for retrieval.
4. **Question Answering**: A prompt template is used to generate concise answers from retrieved context, ensuring accurate and short responses.
5. **Cost Estimation**: The system calculates and prints the cost of each query based on OpenAI’s pricing for prompt and completion tokens.

## Workflow

1. Load documents from a specified web source.
2. Split documents into smaller chunks for efficient processing.
3. Embed documents and store them in a vector store using FAISS.
4. Use a retriever to fetch relevant document chunks based on the query.
5. Generate an answer to the query using GPT-3.5-turbo, and track the cost associated with the query execution.
   
## How to Use

1. **Environment Setup**: Use `.env` to securely store and load your OpenAI API key.
2. **Document Loading**: Documents are loaded from a provided URL (e.g., LangSmith documentation) and processed into manageable chunks.
3. **Run Queries**: Input a query (e.g., “What is LangSmith?”) to retrieve relevant context and generate an answer.
4. **Monitor Costs**: The project tracks API costs for both prompt and completion tokens.

## Installation

1. Clone the repository.
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Set up your `.env` file with your OpenAI API key:
   ```bash
   OPENAI_API_KEY=your_openai_api_key
   ```
4. Run the system to input queries and generate answers.

## License

This project is licensed under the MIT License.

---

This `README.md` provides a clear overview of your project’s functionality and setup, focusing on key components and usage instructions without including the actual code.

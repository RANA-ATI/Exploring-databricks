# Databricks Inferencing Serving Endpoints

**This project demonstrates how to use Databricks for serving machine learning models with OpenAI integration, focusing on embedding-based retrieval and querying. We often need to pass raw prompt template without any need to compel with convention, which imo we cannot do with openai databricks API but that is possible with langchain. It includes the process of setting up a vector database using ChromaDB, creating embeddings, and performing inference using both OpenAI and Langchain methods.**

## Features
- **```Integration with OpenAI```**: Uses OpenAI's API to perform inference and generate responses based on embedded data.
- **```Embedding Storage with ChromaDB```**: Stores and retrieves embeddings using ChromaDB for efficient query processing.
- **```Custom Text Chunking```**: Splits and processes large text documents into manageable chunks to ensure effective embedding.
- **```Support for Multiple Query Methods```**: Provides options for querying data using OpenAI's LLMs as well as Langchain's capabilities.

## Requirements
- Python 3.10
- Databricks account and endpoint
- ChromaDB
- OpenAI API key
- Libraries: `openai`, `chromadb`, `pypdf`, `langchain_databricks`

## Setup
1. **Clone the Repository**: Clone this repository to your local machine.
2. **Environment Setup**: Set up the required environment variables such as `OPENAI_API_KEY` and `DATABRICKS_ENDPOINT`.
3. **Install Dependencies**: Install the necessary Python packages using `pip install -r requirements.txt`.
4. **Configure Database**: Initialize ChromaDB and create a collection to store embeddings.

## Workflow
1. **Data Preparation**: Extracts text from documents (e.g., PDFs) and processes it into chunks for embedding.
2. **Embedding Creation**: Generates embeddings for text chunks using Sentence Transformer models.
3. **Store Embeddings**: Saves the generated embeddings into a ChromaDB collection for efficient retrieval.
4. **Query Processing**: Retrieves relevant document chunks based on user queries.
5. **Inferencing**: Uses either OpenAI's LLM or Langchain models to provide context-specific answers based on the retrieved information.

## Usage
- **Embedding and Storing Data**: Upload text-based documents, generate embeddings, and store them in the vector database.
- **Querying with OpenAI**: Use OpenAI's API to query the database and get answers based on the embedded data.
- **Querying with Langchain**: Alternatively, leverage Langchain models for querying and analyzing the stored data.

## Benefits
- **Learning**: We often need to pass raw prompt template without any need to compel with convention, which imo we cannot do with openai databricks API but that is possible with langchain.
- **Scalable**: Can handle large volumes of text data and efficiently manage embeddings.
- **Customizable**: Supports different chunking strategies for text processing, making it adaptable to various document types.
- **High Accuracy**: Uses state-of-the-art language models like Llama 3.1 to ensure accurate and contextually relevant responses.

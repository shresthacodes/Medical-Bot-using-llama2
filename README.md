# MediBot

## Chat bot for enthuastic medical students

This project implements a question-answering system for medical queries using PDF documents as the knowledge base. It leverages large language models (Llama 2) and vector stores for efficient retrieval and answering. It uses LangChain for natural language processing tasks and ChainLit for chatbot functionality.

## Features

- PDF document ingestion and processing
- Vector store creation for efficient information retrieval
- Question-answering using a fine-tuned large language model(Llama 2)
- Interactive chat interface

## Setup

### Installation

1. Clone this repository:
   ```sh
   git clone https://github.com/esha1231/Medical-Bot-Llama-2.git
   cd Medical-Bot-Llama-2
   ```
2. Install the required packages:
   ```sh
   pip install PyPDF
   pip install langchain
   pip install -U langchain-community
   pip install torch
   pip install accelerate
   pip install bitsandbytes
   pip install ctransformers
   pip install sentence-transformers
   pip install faiss-cpu
   pip install huggingface_hub
   pip install chainlit
   ```
3. Download the Llama 2 model:

- Obtain the `llama-2-7b-chat.ggmlv3.q8_0.bin` file and place it in the project directory.

4. Prepare your data:

- Place your PDF documents in the `data/` directory.

## Usage

1. Ingest the documents and create the vector store:
   ```sh
   python main.py
   ```
2. Start the chat interface:
   ```sh
   chainlit run model.py -w
   ```
3. Interact with the bot through the provided chat interface.

## Project Structure

- `ingest.py`: Script for processing PDF documents and creating the vector store.
- `model.py`: Defines the QA model and chat interface.
- `data/`: Directory to store input PDF documents.
- `vectorstore/db_faiss`: Directory where the FAISS vector store is saved.

## Dependencies

Main libraries used in this project:

- langchain
- PyTorch
- Hugging Face Transformers
- FAISS
- Chainlit

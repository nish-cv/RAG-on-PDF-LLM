# RAG Application 

This project involves a Python application that extracts data from a PDF (Also supports multiple PDFs), stores its embeddings in a vector database, and uses those embeddings to answer prompts given to a language model (RAG).

## Installation

To get started, you need to install the following Python libraries. You can install them using `pip`:

```bash
pip install torch
pip install langchain
pip install langchain-community
pip install pinecone
pip install pymupdf
pip install transformers
pip install dotenv #To store env variables (Optional)
```
And to get the bitsandbytes library for quantization
```bash
git clone https://github.com/TimDettmers/bitsandbytes.git && cd bitsandbytes/
pip install -r requirements-dev.txt
cmake -DCOMPUTE_BACKEND=cuda -S .
cmake --build . --config Release
python -m build --wheel
```
## LLM used
[meta-llama/Meta-Llama-3-8B](https://huggingface.co/meta-llama/Meta-Llama-3-8B)

## Authentication

### Hugging Face

To use the Hugging Face model, you need to authenticate. You can obtain the `HF_AUTH` code by requesting it from the Hugging Face website:

1. Go to the [Hugging Face website](https://huggingface.co/).
2. Sign up or log in to your account.
3. Navigate to your account settings to create a new API token.

### Pinecone

You will also need an API key for Pinecone. You can create a free Pinecone account and generate an API key:

1. Go to the [Pinecone website](https://www.pinecone.io/).
2. Sign up for a free account.
3. After logging in, navigate to the API section to create a new API key or use the default.

## Usage

Once you have installed the necessary libraries and configured your API keys, you can run the application as shown in the notebook. Make sure to replace the placeholder values for `HF_AUTH` and `PINECONE_API_KEY` with your actual credentials.

## Contributing

If you would like to contribute to this project, please feel free to fork the repository and submit a pull request. 

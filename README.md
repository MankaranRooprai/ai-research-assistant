# AI Research Assistant

AI Research Assistant is a Python-based tool that utilizes state-of-the-art natural language processing (NLP) models to assist in generating detailed research papers on specific topics using the latest news articles. This assistant integrates AI techniques for document retrieval, similarity-based search, and text generation to produce a comprehensive research paper. 

## Features

- **AI-Powered Content Generation**: Uses GPT-based models (e.g., GPT-Neo) to generate well-structured research papers based on real-time data.
- **Article Retrieval**: Retrieves relevant news articles using the News API and uses them as a context for the research paper.
- **Similarity Search**: Applies FAISS (Facebook AI Similarity Search) for efficient similarity-based document retrieval.
- **Customizable Querying**: Allows for customized queries to search for articles, such as "AI in healthcare".
- **Coherent and Structured Output**: Outputs papers with an introduction, body, conclusion, and references based on the input data.

## Installation

### Prerequisites

Before using this tool, ensure you have the following dependencies installed:

- Python 3.7+
- Hugging Face `transformers` library for pre-trained models.
- `sentence-transformers` for generating document embeddings.
- `faiss` for similarity search.
- `requests` for fetching news articles.

To install the necessary Python libraries, run:

```bash
pip install transformers sentence-transformers faiss-cpu requests
```
## Setup

Hugging Face API Token: Sign up at Hugging Face and obtain your API token. Set the token in your environment variables.

```bash
export HF_AUTH_TOKEN="your_hugging_face_token"
```

News API Key: Register at NewsAPI to fetch relevant articles.

```bash
export NEWS_API_KEY="your_news_api_key"
```

## Usage

- **Fetch Articles**: The assistant fetches relevant news articles based on the provided query (e.g., "AI in healthcare") using the News API. Only the titles and descriptions are fetched (article content is a premium).
  
- **Document Embedding**: The fetched documents are embedded using the SentenceTransformer model (all-mpnet-base-v2).
  
- **FAISS Indexing**: A FAISS index is created to perform efficient similarity-based search over the document embeddings.
  
- **Query Embedding**: The input query (e.g., "AI in healthcare") is embedded and used to find the top relevant documents using FAISS search.
  
- **Text Generation**: Based on the top retrieved documents, a prompt is constructed, and a GPT-based model (e.g., GPT-Neo) is used to generate a research paper.
  
- **Output**: The output is SUPPOSED to be structured research paper, including an introduction, body, and conclusion, with references derived from the news articles. But the model insists on giving us the instructions rather than generate the research paper itself. A better model like ChatGPT was not used as it costs money.

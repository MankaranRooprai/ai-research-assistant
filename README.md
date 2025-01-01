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

# Amazon Fashion Search Engine

This project is a fashion product search engine using Elasticsearch and sentence embeddings. It allows users to search for Amazon fashion products based on semantic similarity, making it easy to find relevant products by analyzing the meaning of search terms.

## Project Overview

The project consists of three main steps:

1. **Index Mapping Setup**: Creates the Elasticsearch index structure for fashion products. This structure defines the data types and configures the `DescriptionVector` as a dense vector field, allowing for similarity search with vector embeddings.

2. **Data Loading and Indexing**: Loads product data from a CSV file, processes the descriptions into sentence embeddings, and stores them in Elasticsearch.

3. **Search and User Interface**: Provides a Streamlit-based UI where users can enter a search term, which is transformed into a vector and matched against product descriptions in Elasticsearch, returning the most relevant products.

## Key Components

- **indexMapping**: Defines the structure of the Elasticsearch index, with fields like `ProductID`, `ProductName`, and `DescriptionVector`.
- **Data Ingestion and Vectorization**: Reads product data from a CSV file, applies sentence embeddings on descriptions using the `SentenceTransformer` model, and indexes the products in Elasticsearch.
- **Search Engine**: Accepts a search term from the user, converts it to a vector, and performs a k-nearest neighbor (KNN) search in Elasticsearch to retrieve relevant products.

## Requirements

To run this project, you will need the following libraries:

- `pandas`
- `sentence_transformers`
- `elasticsearch`
- `streamlit`
- `ssl`
- `certifi`
# Persian Text Processing and Information Retrieval System

This Python script demonstrates a comprehensive approach to processing Persian text and implementing an information retrieval system. The code is structured into several sections, each handling a different aspect of the text processing and information retrieval tasks. Below is a brief overview of each section and its functionality:

## Features

### Reading From File
- **Purpose**: Loads JSON data from a file, handling common errors such as file not found and JSON decoding errors.
- **Dependencies**: `json`

### Document Preprocessing
- **Purpose**: Normalizes and tokenizes Persian text, including sentence tokenization with consideration for numerical values and various punctuation marks. Implements corrections for spacing and unwanted characters, and applies stemming and stopword removal.
- **Dependencies**: `parsivar`, `hazm`, `re`, `typing`

### Positional Indexing
- **Purpose**: Creates a positional index for the preprocessed documents, allowing for efficient retrieval of documents based on term positions within the text.
- **Dependencies**: `collections.defaultdict`

### Vectorizing
- **Purpose**: Converts documents into TF-IDF vectors, facilitating the comparison and retrieval of documents based on their content similarity.
- **Dependencies**: `math`, `numpy`, `scipy.sparse`

### Create Champion List
- **Purpose**: Generates champion lists for terms to optimize the retrieval process by limiting the search space to the most relevant documents.
- **Dependencies**: `heapq`

### Answer Queries
- **Purpose**: Implements functions to answer user queries by calculating cosine similarities between query vectors and document vectors, with optimizations through index elimination and champion lists.
- **Dependencies**: `numpy`

### Data Persistence
- **Purpose**: Demonstrates how to serialize and store the positional index using `pickle`, allowing for data to be saved and loaded efficiently.

## Instructions

1. Ensure all dependencies are installed.
2. Place your dataset in the same directory as the script or modify the file path accordingly.
3. Run the script to preprocess the documents, build the positional index, and test query processing capabilities.
4. Use the provided functions to experiment with different queries and observe the system's performance.

## Requirements

- Python 3.x
- `parsivar` library for Persian text normalization and tokenization.
- `hazm` library for stopwords list.
- `numpy` and `scipy` for vector operations and sparse matrix representation.

## Dataset

The script expects a JSON file (`IR_data_news_5k.json`) containing Persian text documents. Each document should have a unique identifier and contain textual content for processing and indexing.

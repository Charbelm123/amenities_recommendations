# Amenities Recommendation System

A smart recommendation system for hotel amenities using vector embeddings and semantic search capabilities. The system supports multiple search approaches including BM25, hybrid, and vector-based similarity search.

## Features

- Text embeddings using Sentence Transformers
- Multiple search strategies:
  - BM25 text search
  - Hybrid search (combines text and vector search)
  - Vector similarity search
- Spell checking for user queries
- Support for both Elasticsearch and Weaviate backends
- Docker containerization

## Tech Stack

- Python 3.10+
- Elasticsearch 8.14.3
- Weaviate 1.27.0
- Sentence Transformers (all-mpnet-base-v2 model)
- Docker & Docker Compose

## Getting Started

### Prerequisites

- Python 3.10+
- Docker and Docker Compose
- Virtual environment (recommended)

### Installation

1. Clone the repository
2. Create and activate a virtual environment:

```sh
python -m venv .venv
source .venv/bin/activate  # Linux/Mac
.venv\Scripts\activate     # Windows

3- install dependatices
pip install -r requirements.txt

4-Start the services using Docker Compose:
docker-compose up -d

Usage:
The system provides two main notebooks:

amenities_rec.ipynb - Elasticsearch implementation
amenities_recommendations.ipynb - Weaviate implementation

Both notebooks demonstrate:

Loading and processing amenities data
Creating vector embeddings
Setting up search indices
Performing various types of searches
Data Structure

Amenities are stored with the following information:
ID
Name
Description
Categories
Price
Vector embeddings for various fields
Search Methods
BM25 Search: Traditional keyword-based search
Hybrid Search: Combines keyword and semantic similarity
Vector Search: Uses semantic similarity based on embeddings
Configuration
Elasticsearch configuration in docker-compose.yml
Weaviate configuration in docker-compose.yml
Vector dimensions: 768 (from all-mpnet-base-v2 model)


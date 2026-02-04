# Semantic Book Recommendation Chatbot

A web-based chatbot that provides intelligent book recommendations using **Natural Language Processing (NLP)** and **Vector Similarity Search**. Instead of simple keyword matching, this system understands the semantic context of a user's query—such as themes, character types, or plot descriptions—to find the best matches from a dataset of 5,000+ books.

## Overview
This project was developed as part of my coursework at **Ukrainian Catholic University**. It bridges the gap between raw data and user experience by implementing a **Sentence Transformer** model to encode text into high-dimensional vectors, which are then indexed using **FAISS** for lightning-fast retrieval.

## Tech Stack
* **Backend:** Python, Flask
* **Machine Learning:** Sentence-Transformers (`all-MiniLM-L6-v2`), FAISS (Facebook AI Similarity Search)
* **Data Handling:** Pandas, NumPy
* **NLP:** NLTK (Stopword removal)
* **Frontend:** HTML5, CSS3 (Custom responsive UI)

## Key Features
* **Semantic Understanding:** Uses `all-MiniLM-L6-v2` to process queries, allowing users to find books by describing themes (e.g., "dystopian rebellion") rather than just titles.
* **Dynamic Embedding Logic:** The system intelligently prioritises specific columns (Description, Characters, Author, etc.) based on keywords detected in the user's natural language input.
* **High-Performance Search:** Utilizes a `FAISS IndexFlatL2` for efficient similarity searching across thousands of records.
* **Responsive Chat Interface:** A clean, user-friendly web interface with a professional, minimalist aesthetic.
* **Data Prioritisation:** The engine sorts the dataset by user rating before indexing, ensuring that the recommendations provided are not only relevant but also highly regarded by the community.
* **Scalability:** By using a vector index instead of a traditional relational database LIKE query, the system remains performant and scalable as the dataset grows.
* **Feature Engineering:** Implemented custom stopword filtering to remove domain-specific noise (e.g., "book", "writer"), significantly improving the signal-to-noise ratio in search results.

## How to Run
1. Install dependencies:

```
pip install flask pandas numpy faiss-cpu sentence-transformers nltk
```
2. Run the application:
   
```
python app.py
```

3. Access the bot: Navigate to http://127.0.0.1:5000/main in your browser.

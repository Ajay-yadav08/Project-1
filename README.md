# 🎬 Content-Based Movie Recommender System using Cosine Similarity

This project implements a content-based movie recommendation system that suggests similar movies based on the content features (such as genres, keywords, cast, and crew) of a selected movie. It uses **cosine similarity** to measure the similarity between movies.

## 📌 Features

- Content-based filtering using metadata (genres, cast, crew, keywords)
- Cosine similarity for measuring movie similarity
- Suggests top N similar movies based on a user-selected movie
- Clean and simple code, easy to integrate with front-end applications

## 📁 Dataset

The system uses metadata from [The Movie Database (TMDb)](https://www.themoviedb.org/) which typically includes:

- `movies_metadata.csv`
- `credits.csv`
- `keywords.csv`

These datasets contain information such as:

- Movie titles
- Overview
- Cast & Crew
- Genres
- Keywords

## 🛠️ How It Works

1. **Data Preprocessing:**
   - Merge datasets on `movie_id`
   - Extract relevant fields (title, overview, genres, keywords, cast, director)
   - Clean and normalize text data

2. **Feature Engineering:**
   - Create a "soup" of relevant content features
   - Vectorize text data using `CountVectorizer` or `TfidfVectorizer`

3. **Similarity Calculation:**
   - Compute cosine similarity between all movie vectors

4. **Recommendation Function:**
   - Given a movie title, return the top N most similar movies based on cosine similarity

## 🚀 Getting Started

### Prerequisites

- Python 3.7+
- pandas
- numpy
- scikit-learn

Install dependencies:

```bash
pip install pandas numpy scikit-learn

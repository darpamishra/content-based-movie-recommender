# content-based-movie-recommender

## Overview
This repository implements a content-based movie recommendation system using the TMDB 5000 Movie Dataset. By analyzing metadata such as genres, keywords, cast, and crew, the system identifies and recommends movies with similar attributes using cosine similarity.


## Dataset

### The dataset includes:

- tmdb_5000_movies.csv: Contains information on movie metadata such as title, genres, overview, budget, and revenue.
- tmdb_5000_credits.csv: Includes information about the cast and crew for each movie.

These datasets are merged to form a comprehensive dataset for building the recommendation system.


## Features

- Extracts and preprocesses key features like genres, keywords, cast, and crew from the dataset.
- Creates a unified "tags" column by combining processed metadata.
- Uses Porter Stemming for reducing words to their base form.
- Implements Count Vectorization for text feature representation.
- Computes cosine similarity to find and rank similar movies.
- Provides a simple recommendation function to suggest similar movies.



# Methodology

## Steps:

### Data Cleaning:

- Dropped missing and duplicate values.
- Extracted only relevant columns (movie_id, title, genres, keywords, cast, crew, overview).

### Feature Engineering:

- Converted JSON-like columns (e.g., genres, keywords, cast, crew) into list representations.
- Retained top 3 cast members and identified the director.
- Preprocessed overview into tokenized words.

### Tag Creation:

- Combined overview, genres, keywords, cast, and crew into a single tags column.

### Vectorization and Similarity:

- Used CountVectorizer to convert text data into numerical vectors.
- Computed cosine similarity to measure the similarity between movies.

### Recommendation System:

- Developed a function to recommend movies based on similarity.


## Dependencies

- Python 3.x
- NumPy
- Pandas
- scikit-learn
- NLTK

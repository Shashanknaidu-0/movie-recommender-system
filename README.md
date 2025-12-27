# Movie Recommender System 🎬

A Content-Based Movie Recommender System built with Python. This project uses machine learning to suggest movies similar to a user's choice by analyzing metadata such as genres, keywords, cast, and directors.

## 🚀 How it Works
The system leverages **Cosine Similarity** to find the relationship between movies based on their features.

1.  **Feature Selection**: The system extracts key attributes: `keywords`, `cast`, `genres`, and `director`.
2.  **Data Preprocessing**: Missing values in these features are filled with empty strings to ensure the algorithm runs smoothly.
3.  **Feature Combination**: All selected features are combined into a single string for each movie.
4.  **Vectorization**: The combined text is converted into a count matrix using `CountVectorizer`.
5.  **Similarity Calculation**: A cosine similarity matrix is computed from the count matrix to find movies with the most similar text profiles.
6.  **Recommendation**: The system identifies the index of a chosen movie (e.g., "Avatar") and returns the top 50 most similar titles in descending order of similarity score.

## 🛠️ Tech Stack
- **Language:** Python
- **Data Analysis:** Pandas, NumPy
- **Machine Learning:** Scikit-learn (`CountVectorizer`, `cosine_similarity`)

## 📁 Dataset
The project uses `movie_dataset.csv`, which contains detailed information on approximately 4,800 movies, including:
- **Title**: The name of the movie.
- **Genres**: Action, Adventure, Fantasy, etc.
- **Cast**: Lead actors.
- **Director**: The film's director.
- **Keywords**: Tags related to the movie's plot (e.g., "culture clash", "future").

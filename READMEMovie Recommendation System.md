# Movie Recommendation System

This repository contains code for building a movie recommendation system based on genre similarity using Python and scikit-learn.

## Introduction

Movie recommendation systems are widely used in the entertainment industry to provide personalized movie recommendations to users. These systems are built on the idea of finding similarities between movies and recommending movies that are similar to the ones a user has already watched or liked.

In this project, we'll focus on building a movie recommendation system based on genre similarity. The idea is to recommend movies to a user based on the genres of movies they have liked. We will use a dataset containing information about movies, including their titles, genres, actors, directors, release years, and ratings.

## Prerequisites

Before running the code in this repository, make sure you have the following libraries installed:

- Pandas
- scikit-learn

You can install these libraries using pip:

```
pip install pandas scikit-learn
```

## Code Overview

Here's an overview of the main steps in the code:

1. **Load and Preprocess Dataset**: The dataset containing information about movies is loaded and any duplicate rows are removed. Categorical columns like genres, actors, and directors are one-hot encoded to prepare the data for similarity calculation.

2. **Feature Engineering**: Feature engineering involves creating a TF-IDF (Term Frequency-Inverse Document Frequency) matrix for the genres. This matrix is used to calculate the cosine similarity between movies based on their genres.

3. **Calculate Similarity**: Cosine similarity is calculated for genres, creating a similarity matrix. This matrix represents how similar movies are to each other based on their genres.

4. **Get Recommendations**: A function is defined to get movie recommendations for a given movie title. It takes into account the cosine similarity scores and returns the top 3 recommended movies based on genre similarity.

## How to Use

To use this code, follow these steps:

1. Clone this repository to your local machine.

2. Make sure you have the required libraries installed (Pandas and scikit-learn).

3. Replace the `dataset.csv` file with your own dataset if needed. The dataset should have columns for movie titles, genres, actors, directors, release years, and ratings.

4. Run the Python script to load, preprocess, and calculate movie recommendations based on genre similarity.

5. Use the `get_genre_recommendations` function to get recommendations for a specific movie title.

6. Customize the number of recommendations and other parameters as needed.


# Get recommendations for a movie titled "Inception"
recommended_genre_movies = get_genre_recommendations("Inception", cosine_sim_genres)

# Print the recommended movies
print(recommended_genre_movies)
```

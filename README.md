## Movie Recommendation System

This project is a simple movie recommendation system built using Python, pandas, scikit-learn, and streamlit. It provides movie recommendations based on a selected film's content, including its genres, keywords, cast, and crew.

## Project Overview

The recommendation system analyzes movie metadata to find similarities between films. It uses a cosine similarity algorithm to measure the likeness of one movie to another based on a consolidated tags column. This single column is created by combining the movie's overview, genres, keywords, cast, and crew.

The system processes the data in the following key steps:

***1. Data Preprocessing***: The raw movie data from the TMDB 5000 dataset is cleaned, and stringified JSON columns (e.g., genres, cast) are converted into usable lists.

***2. Feature Engineering***: A new tags column is created by merging the text from the movie's overview, genres, keywords, cast, and crew. This becomes the primary feature for the recommendation model.

***3. Text Vectorization***: The tags text data is converted into numerical vectors using CountVectorizer. This process transforms the text into a format that a machine learning model can understand.

***4. Stemming***: A Porter Stemmer from the nltk library reduces words to their root form (e.g., "loving" and "loved" both become "love"). This enhances the accuracy of the vectorization.

***5. Similarity Calculation***: The cosine_similarity function calculates the similarity between each movie's vector and all others, creating a similarity matrix that is the core of the recommendation engine.

***6. Web Application***: A user-friendly web interface is built with Streamlit, allowing users to select a movie and receive instant recommendations.

## How to Run the Project
**Prerequisites**:

To run this project, you need to have Python installed. You can install all the required libraries using pip:

pip install pandas scikit-learn streamlit nltk

***Files Needed***:

You need the following files in the same directory:

1. tmdb_5000_movies.csv

2. tmdb_5000_credits.csv

3. app.py (The Streamlit application code)

4. movies_dict.pkl (Generated after running the data processing script)

5. similarity.pkl (Generated after running the data processing script)

5. To generate the .pkl files, you must first run the data processing script (the Python code provided in the first block). The streamlit app will not work without these two files.

**Running the Application:**

1. Place all the necessary files in the same folder.

2. Open your terminal or command prompt.

3. Navigate to the directory where your files are located.

4. Run the Streamlit application with the following command:

5. streamlit run app.py 

6. Your default web browser will open a new tab with the Movie Recommendation System running.

## AUTHOR:
**Okonji Chukwunonyelim Gabriel**
  
ML Engineer/ Data Scientist

CONTACT: nonnyokonji@gmail.com


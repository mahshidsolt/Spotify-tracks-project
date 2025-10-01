# Spotify-tracks-project
1. Project Overview

A content-based music recommendation system using the Spotify Tracks Dataset.
Users can select a song and get top N similar tracks based on audio features and genre.

Features used for recommendations:

Numeric audio features: danceability, energy, valence, tempo, loudness, etc.

Track genres (one-hot encoded)

Goal:
Build a lightweight, interactive web app using Streamlit that recommends similar songs.

2. Dataset

Source: Spotify Tracks Dataset on Kaggle

Cleaning & preprocessing steps:

Removed irrelevant columns (e.g., album info, track ID)

Handled missing values

Deduplicated tracks

One-hot encoded track_genre

Scaled numeric features for similarity calculation

3. How It Works

Load preprocessed dataset.

Combine scaled numeric features and one-hot encoded genres into a single feature vector.

Compute cosine similarity between all tracks.

When a user selects a track in the app, return the top N most similar tracks.

4. Installation & Requirements

Python version: 3.x

Required libraries:

pandas
numpy
scikit-learn


Install via pip:

pip install pandas numpy scikit-learn streamlit

5. Running the App

Make sure spotify_clean.csv (cleaned dataset) is in the project folder.



Select a song from the dropdown to see recommendations.

6. Sample Output
Input song: "Blinding Lights — The Weeknd"
Recommended songs:
- "Save Your Tears — The Weeknd"
- "Don’t Start Now — Dua Lipa"
- "Circles — Post Malone"
- "Levitating — Dua Lipa"
- "Physical — Dua Lipa"

7. Future Improvements

improve the app on streamlit to give it user interface

improve the searching options

Allow multi-genre filtering.

Integrate Spotify API to play previews of recommended songs.

Implement user-based collaborative filtering if user data is available.

8. Acknowledgements

Dataset: Spotify Tracks Dataset by Maharshi Pandya

Tools: Python, Pandas, Scikit-learn

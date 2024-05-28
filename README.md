# Spotify-API-Music-RS

## Song Recommendation System

This project is a song recommendation system that uses Fuzzy C-means clustering and cosine similarity to recommend songs based on a user's input. The system also provides recommendations for songs that are the opposite of the input song. The frontend is built with HTML and Flask, providing an interactive web interface for users to input their song and receive recommendations.

## Features
- **Song Recommendation**: Recommends songs similar to a user-specified song based on audio features.
- **Opposite Song Recommendation**: Suggests songs that are least similar to a user-specified song.
- **Interactive Web Interface**: Built using Flask and HTML for easy user interaction.

## Dependencies
- Python 
- Pandas
- NumPy
- fcmeans
- scikit-learn
- Flask

## Installation
1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/Spotify-API-Music-RS.git
    cd Spotify-API-Music-RS
    ```

2. Install the required packages:
    ```bash
    pip install -r requirements.txt
    ```

3. Run the Flask app:
    ```bash
    python app.py
    ```

4. Open your web browser and go to `http://127.0.0.1:5000/`.

## Code Overview
The main code is structured to include two core functionalities: song recommendations and opposite song recommendations.

### Key Functions
- `recommend_songs(song_name)`
  - Reads audio features from `data.csv`.
  - Performs Fuzzy C-means clustering.
  - Recommends songs based on cosine similarity.

- `opposite_songs(song_name)`
  - Reads audio features from `data.csv`.
  - Performs Fuzzy C-means clustering.
  - Recommends songs that are least similar based on cosine similarity.

### Flask Routes
- `index()`
  - Renders the main HTML page.

- `get_recommendations()`
  - Handles AJAX requests to get song recommendations.

- `get_opposite_songs()`
  - Handles AJAX requests to get opposite song recommendations.

## File Structure

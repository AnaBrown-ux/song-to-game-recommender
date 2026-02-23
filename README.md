# 🎵 Song-to-Game Recommender

A Flask web application that recommends video games based on your music taste. Enter a song and artist, and the app maps your music genre to a compatible game genre, then surfaces real game recommendations with current pricing and deal data.

---

## How It Works

1. User enters a song title and artist name
2. The app queries the **Spotify API** to identify the music genre associated with that artist
3. A custom genre-mapping algorithm translates the music genre into a compatible video game genre (e.g. rock → action/shooter)
4. The app queries the **RAWG API** to fetch top-rated games in that genre
5. Current pricing and deals for those games are retrieved from the **CheapShark API**
6. Results are displayed in a clean, styled interface

---

## Features

- OAuth 2.0 authentication flow with the Spotify API
- Cross-domain genre mapping across 11+ music categories
- Real-time game pricing and deal data
- Responsive front-end with custom CSS styling
- Aggregates data from 20+ game entries per query

---

## Tech Stack

- **Backend:** Python, Flask
- **APIs:** Spotify Web API, RAWG Video Games Database API, CheapShark API
- **Frontend:** HTML, CSS (Jinja2 templating)
- **Networking:** Python `urllib` library

---

## Setup & Installation

### Prerequisites
- Python 3.x
- A [Spotify Developer](https://developer.spotify.com/) account (for API credentials)
- A [RAWG API key](https://rawg.io/apidocs)

### Steps

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/song-to-game-recommender.git
   cd song-to-game-recommender
   ```

2. Install dependencies:
   ```bash
   pip install flask
   ```

3. Create a `keys.py` file in the root directory with your API credentials:
   ```python
   CLIENT_ID = "your_spotify_client_id"
   CLIENT_SECRET = "your_spotify_client_secret"
   RAWG_KEY = "your_rawg_api_key"
   ```

4. Run the app:
   ```bash
   python app.py
   ```

5. Open your browser and go to `http://127.0.0.1:5000`

---

## Screenshots

<img width="590" height="334" alt="Screenshot 2026-02-22 at 7 21 52 p m" src="https://github.com/user-attachments/assets/b2054cb8-f8de-4476-9820-e8d99040a442" />

<img width="590" height="329" alt="Screenshot 2026-02-22 at 7 22 12 p m" src="https://github.com/user-attachments/assets/b117b3d7-91dd-4221-b7d3-a224a1988baf" />

<img width="590" height="326" alt="Screenshot 2026-02-22 at 7 22 33 p m" src="https://github.com/user-attachments/assets/77d7e75b-0c43-47e4-9d30-003fa31e5bf4" />

---

## Collaborators

- [Mariana Moreno](https://github.com/AnaBrown-ux)
- [Dharini Venkatesh](https://github.com/dvenka23)

---

## Acknowledgements

- [Spotify Web API](https://developer.spotify.com/documentation/web-api)
- [RAWG Video Games Database](https://rawg.io/apidocs)
- [CheapShark API](https://www.cheapshark.com/api)

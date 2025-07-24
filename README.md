Chess Analyzer Skeleton
======================

This repository contains a minimal skeleton for a web application that imports
chess games from Lichess and Chess.com and analyzes them to find common
mistakes. The application is split into a **backend** powered by Flask and a
very small **frontend** written in plain HTML/JavaScript.

## Backend

The backend exposes endpoints to import games from Lichess or Chess.com and a
POST endpoint to analyze a list of PGN games. The implementation is mostly a
placeholder so you can build your own heuristics.

### Setup

```bash
cd backend
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
python app.py
```

The server will run on `http://localhost:5000`.

## Frontend

Open `frontend/index.html` in your browser. It allows you to trigger the import
endpoints and paste PGN games for analysis.

## Next Steps

- Implement the API calls in `fetch_lichess_games` and `fetch_chesscom_games`.
- Add real heuristics in `analyze_games` to detect mistakes such as blunders,
  tactical oversights, or suspicious moves.
- Improve the frontend to display statistics more nicely.

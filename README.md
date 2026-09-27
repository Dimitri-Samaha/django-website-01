# Django Website 01

A multi-app Django site bundling a login/registration system with a few small browser games and tools, all served from one project.

## Apps
- **`home`** — user registration, login, logout, and a landing menu (Django's built-in auth system).
- **`madlibs`** — a Mad Libs word-game page.
- **`RockPaperScissors`** — a Rock-Paper-Scissors web game. Game logic lives in `RockPaperScissors/game_logic.py` (kept local to this app rather than importing from the separate `console_games/game_hub` project).
- **`speed_test`** — scaffold for a typing/equation speed test (routes and templates exist; the timing logic itself isn't wired up yet).

## Tech stack
Python, Django, SQLite (default dev database).

## Requirements
```
pip install django
```

## Running it
```
python manage.py migrate
python manage.py runserver
```
Then open http://127.0.0.1:8000/.

## Notes
This project used to reach into a sibling `game_01` folder via `sys.path.append('..')` to reuse its Rock-Paper-Scissors logic. That's been removed — the logic is now copied locally into `RockPaperScissors/game_logic.py` so this project has no dependency outside its own folder.

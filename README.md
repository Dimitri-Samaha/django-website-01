# Django Website 01

A multi app Django site bundling a login and registration system with a few small browser games and tools, all served from one project.

## Apps
- **`home`**: user registration, login, logout, and a landing menu (Django's built in auth system).
- **`madlibs`**: a Mad Libs word game page.
- **`RockPaperScissors`**: a rock paper scissors web game. Its logic lives in `RockPaperScissors/game_logic.py`, kept local to this app rather than imported from the separate `console_games/game_hub` project.
- **`speed_test`**: a scaffold for a typing and equation speed test (routes and templates exist, but the timing logic itself isn't wired up yet).

## Tech stack
Python, Django, and SQLite (the default development database).

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
This project used to reach into a sibling `game_01` folder using `sys.path.append('..')` to reuse its rock paper scissors logic. That's been removed; the logic is now copied locally into `RockPaperScissors/game_logic.py`, so this project has no dependency outside its own folder.

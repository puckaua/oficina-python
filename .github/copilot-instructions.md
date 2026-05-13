# Copilot Instructions for oficina-python

This repository is a small FastAPI + Jinja2 social bingo web app built as a learning workshop.

## Key facts

- Python app targeting `>=3.13`.
- Entry point: `app/main.py`.
- Core backend logic:
  - `app/game_logic.py` — bingo board generation and win detection.
  - `app/game_service.py` — in-memory session state and game actions.
  - `app/models.py` — Pydantic data models and game state enum.
- Frontend templates and HTMX-driven updates live under `app/templates/`.
- Static assets under `app/static/`.
- No external database; per-user session state is stored in a memory dictionary keyed by `session_id`.

## Recommended agent behavior

- Use `uv` commands when available:
  - `uv sync`
  - `uv run pytest`
  - `uv run uvicorn app.main:app --reload --host 0.0.0.0 --port 8000`
- Prefer working with `pyproject.toml` as the source of truth for dependencies and scripts.
- Keep backend changes aligned with the existing session-based game flow.
- When modifying UI behavior, update the Jinja templates and HTMX endpoints together.
- Do not rely on the VS Code simple browser for testing the app; use a normal browser instead.

## Useful files

- `pyproject.toml` — dependency and tooling configuration.
- `app/main.py` — HTTP routes, session handling, and app startup.
- `app/game_logic.py` — game rules and board logic.
- `app/game_service.py` — interactive game session state.
- `tests/` — automated test suite for API and game logic.

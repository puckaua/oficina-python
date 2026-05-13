# AI Agent Instructions for oficina-python

## Development checklist

- [ ] `uv sync`
- [ ] `uv run ruff check .`
- [ ] `uv run pytest`
- [ ] `uv run uvicorn app.main:app --reload --host 0.0.0.0 --port 8000`

This is a small FastAPI + Jinja2 social bingo workshop app. Use `pyproject.toml` for dependencies and keep changes minimal around the HTMX + session flow.

Key files:
- `app/main.py` — routes, sessions, HTMX responses
- `app/game_logic.py` — bingo board and win detection
- `app/game_service.py` — in-memory session state
- `app/templates/` — Jinja2 UI templates

Recommended:
- align frontend changes with endpoint templates,
- run `uv run pytest` before proposing changes,
- test in a real browser, not VS Code simple browser.

Links:
- [README.md](README.md)
- [workshop/](workshop/)

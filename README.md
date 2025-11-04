# FastAPI Calculator

A tiny FastAPI app with unit, integration, and Playwright E2E tests + logging + GitHub Actions CI.

## Quickstart
```bash
pip install -r requirements.txt
python -m playwright install
uvicorn app.main:app --reload
```

Open [http://127.0.0.1:8000](http://127.0.0.1:8000)

## Tests

```bash
pytest -q              # unit + integration
pytest -q -m e2e       # Playwright E2E
```

## CI

CI runs on every push: unit, integration, and e2e. See `.github/workflows/ci.yml`.

## Screenshots to include in submission

1. **GitHub Actions Success** – a green run for the latest commit.
2. **App in Browser** – homepage showing the calculator UI at `http://127.0.0.1:8000`.
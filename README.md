# 🧮 FastAPI Calculator

A FastAPI-based calculator web app demonstrating REST API creation, testing, logging, and CI/CD.
Includes unit, integration, and Playwright end-to-end tests with automated GitHub Actions.

![CI](https://github.com/Tejen1710/FastAPI_calc/actions/workflows/ci.yml/badge.svg)

## 🚀 Quickstart
```bash
# Create virtual environment (optional but recommended)
python -m venv .venv
.\.venv\Scripts\Activate.ps1  # Windows
# or source .venv/bin/activate  # macOS/Linux

# Install dependencies
pip install -r requirements.txt
python -m playwright install

# Run the app
uvicorn app.main:app --reload
```

Open [http://127.0.0.1:8000](http://127.0.0.1:8000) in your browser.
You’ll see a simple calculator UI — enter numbers and choose an operation.

## 🧪 Running Tests
```bash
pytest -q              # Run unit + integration tests
pytest -q -m e2e       # Run Playwright end-to-end tests
```

All tests cover arithmetic logic (add, subtract, multiply, divide) and API endpoints.
E2E tests simulate user interaction with the browser using Playwright.

## 🧾 Logging

The app uses Python’s logging with rotating file output:

Logs are saved in `logs/app.log`

Each request and operation is recorded for debugging and traceability.

## 🔄 Continuous Integration (CI)

Every commit triggers automated testing through GitHub Actions:

- Installs dependencies
- Runs unit, integration, and E2E tests
- Validates the app builds successfully

See the workflow file at `.github/workflows/ci.yml`.
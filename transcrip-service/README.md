# Transcript Service

Minimal FastAPI service placeholder. Current endpoints:
- `GET /health` → `{ "status": "ok" }`.

## Run locally
```
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\\Scripts\\activate
pip install -r requirements.txt
uvicorn app.main:app --host 127.0.0.1 --port 8765 --reload
```

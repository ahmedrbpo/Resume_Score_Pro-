# Resume_Score_Pro

A fullstack project for AI-powered resume scoring and analytics.

## Structure

- `backend/` &mdash; Node.js/Express API with MongoDB for user management, resume uploads, analytics.
- `ai-service/` &mdash; Python FastAPI microservice for resume parsing and scoring.

## Quick Start

### Backend

```bash
cd backend
cp .env.example .env
npm install
npm run dev
```
- Requires MongoDB running (update `MONGO_URI` in `.env`).

### AI Service

```bash
cd ai-service
pip install -r requirements.txt
uvicorn main:app --reload --host 0.0.0.0 --port 8000
```
or with Docker:
```bash
docker build -t ai-service .
docker run -p 8000:8000 ai-service
```

## Integration

The backend calls the AI microservice at `POST /parse-resume`. Make sure both are running for full functionality.

## License

MIT

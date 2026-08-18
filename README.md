# Zerodha (Clone)

This repository is a full-stack clone-style project containing three main services:

- **backend/** – Node.js + Express API that uses MongoDB for storage.
- **frontend/** – React single-page application (public-facing site).
- **dashboard/** – React dashboard app (admin/user dashboard).

What this repo contains
- Dockerfiles for each service and a `docker-compose.yml` to run everything locally.
- A small deployment guide: [README-DEPLOY.md](README-DEPLOY.md#L1).

Quick local run (Docker)
1. Build and start services:
```bash
docker-compose up --build -d
```
2. Open:
	- Backend: http://localhost:3002
	- Frontend: http://localhost:3000
	- Dashboard: http://localhost:3001

Run services locally without Docker
- Backend: `cd backend && npm install && npm start` (set `MONGO_URL` in `.env`)
- Frontend/Dashboard: `cd frontend && npm install && npm start` (and similarly for `dashboard`)

Environment variables
- `MONGO_URL` – MongoDB connection string used by the backend (e.g. `mongodb://mongo:27017/zerodha` for docker-compose).

Notes
- This project was adapted from tutorial code — I removed instructional placeholders and consolidated build/deploy steps in this README and `README-DEPLOY.md`.
- If you want CI/CD, registry publishing, or a production `.env.example`, tell me and I will add it.

License
- See the repository license or add one if you want to open-source this project.


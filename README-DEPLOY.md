Deployment guide

Local container deployment (Docker + Docker Compose):

1. Build and start services:
```
docker-compose up --build -d
```

2. Services will be available at:
- Backend: http://localhost:3002
- Frontend (public site): http://localhost:3000
- Dashboard: http://localhost:3001

3. Notes:
- The backend requires a MongoDB connection string; docker-compose sets `MONGO_URL` to `mongodb://mongo:27017/zerodha` by default.
- To run in production bind to a managed MongoDB and set `MONGO_URL` appropriately.

CI/CD and hosting suggestions:
- For container-based deployment, push images to a registry (GitHub Container Registry, Docker Hub) and deploy using your cloud provider (AWS ECS/EKS, Azure ACI/AKS, GCP Cloud Run, or DigitalOcean App Platform).
- For static frontends consider deploying the `frontend/build` and `dashboard/build` artifacts to Vercel, Netlify, or GitHub Pages.

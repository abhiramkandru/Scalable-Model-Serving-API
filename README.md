# Scalable Model Serving API + Dashboard

FastAPI + TorchServe/TensorRT backend with async micro-batching and Redis cache.
React + Tailwind dashboard for predictions, live SLOs, controls, and request logs.

## Endpoints
- `POST /predict` → `{ prediction, model_version, latency_ms, batch_id }`
- `GET /healthz` → `{ status }`
- `GET /metrics` → Prometheus text
- `POST /config` → `{ batch_ms?, batch_size?, enable_cache?, shadow_percent?, active_model? }`

## Quick start
```bash
make dev   # runs backend + frontend via docker-compose


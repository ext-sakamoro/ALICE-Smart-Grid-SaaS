# ALICE-Smart-Grid

Real-time power grid monitoring, prediction, and optimization platform

## License

AGPL-3.0

## Architecture

```
Frontend :3000  -->  API Gateway :8080  -->  Core Engine :8081
```

| Layer | Port | Technology |
|-------|------|-----------|
| Frontend | 3000 | Next.js 14, Tailwind CSS |
| API Gateway | 8080 | Rust, Axum |
| Core Engine | 8081 | Rust, Axum |

## ALICE Crate Integration

alice-energy, alice-cache, alice-semantic-telemetry, alice-analytics

## Endpoints

| Method | Path | Description |
|--------|------|-------------|
| `POST` | `/api/v1/grid/simulate` | 電力グリッドシミュレーション |
| `GET ` | `/api/v1/grid/status` | リアルタイムグリッド状態 |
| `POST` | `/api/v1/grid/dispatch` | 経済的負荷配分最適化 |
| `GET ` | `/api/v1/grid/alerts` | 異常検知アラート |
| `GET ` | `/health` | ヘルスチェック |

## Quick Start

```bash
cd services/core-engine
cargo run --release
curl http://localhost:8081/health
```

## Author

Moroya Sakamoto

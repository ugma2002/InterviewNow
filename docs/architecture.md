# InterviewNow — Architecture (Planned)

```mermaid
flowchart LR
  U[User Browser\nReact + Monaco + WebRTC] -- HTTP / WebSocket --> API[Backend API\n(Node.js/Express or FastAPI)]
  API -- SQL --> DB[(PostgreSQL)]
  API -- cache/queue --> R[(Redis)]
  U <-- WebRTC Peer --> P[Peer User]
  API <-- OAuth --> OA[GitHub/Google Auth]
  API -- logs/metrics --> M[Monitoring\nGrafana/CloudWatch]

# InterviewNow – Real-Time Interview Simulation Platform

## ✨ Highlights
- Peer-to-peer skill-based matching for interview practice  
- Live coding with Monaco Editor (multi-language, test cases)  
- Built-in video/voice integration via WebRTC  
- Structured feedback forms for peer evaluation  
- Progress tracking with practice logs and gamification  

## 🧱 Tech Stack
**Frontend:** React, Tailwind CSS, Redux Toolkit  
**Backend:** Node.js (Express) or FastAPI  
**Realtime:** WebRTC (video/voice) + Socket.IO  
**Database:** PostgreSQL + Redis (sessions, queues)  
**Code Editor:** Monaco Editor (VS Code style)  
**Auth:** OAuth (GitHub/Google) + JWT  
**Deployment:** Vercel (frontend), Render/Heroku (backend)  

## 🗺️ Architecture (planned)
```mermaid
flowchart LR
  U[User Browser\nReact + Monaco + WebRTC] -- HTTP/WS --> B[Backend API (Node/FastAPI)]
  B -- SQL --> D[(PostgreSQL)]
  B -- cache/queue --> R[Redis]
  U <-- WebRTC --> P[Peer User]
  B -- OAuth --> A[GitHub/Google Auth]
  B -- logs --> M[Monitoring (Grafana/CloudWatch)]


planned Structure

/frontend   # React + Monaco Editor
/backend    # Node/FastAPI APIs
/docs       # screenshots, diagrams

Screenshots

![InterviewNow Architecture](docs/architecture.png)

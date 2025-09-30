# Server Dashboard

A comprehensive server monitoring dashboard that displays real-time CPU, memory, and system metrics with both Python backend and Svelte frontend.

## Features

- 📊 Real-time server metrics (CPU, memory, disk usage)
- 🌐 Network scanning and port detection
- 🔍 System process monitoring
- 📈 Historical data tracking
- 📱 Responsive web interface
- ⚡ Fast API with WebSocket support

## Tech Stack

- **Python + FastAPI** - Backend API with real-time capabilities
- **SvelteKit** - Frontend framework
- **TailwindCSS** - Utility-first styling
- **WebSocket** - Real-time data streaming
- **Nmap** - Network scanning capabilities
- **Glances** - System monitoring integration

## Requirements

- **Nmap** - Install using your package manager
- **Glances** - Running in webserver mode (backend connects to its endpoints)
- **Note:** Server component requires root privileges for network scanning

## Getting Started

### Prerequisites

- Python 3.8+
- Node.js (v16 or higher)
- Nmap and Glances installed
- Root privileges for server component

### Installation

1. **Backend Setup:**
```bash
cd server
python3 -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
chmod +x main.py
./main.py
```

2. **Frontend Setup:**
```bash
cd client
pnpm install
pnpm run dev --host
```

3. Access the application:
   - Frontend: `http://localhost:5173`
   - Backend API: `http://localhost:8000`

## Building for Production

### Frontend
```bash
cd client
pnpm run build
```

### Backend
The Python backend is ready for deployment to any WSGI-compatible server.

## Deployment

- **Frontend**: Deploy to Vercel, Netlify, or any static hosting
- **Backend**: Deploy to VPS, Railway, Render, or similar Python hosting
- **Database**: SQLite for development, PostgreSQL recommended for production

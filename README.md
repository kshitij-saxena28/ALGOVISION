# ALGOVISION.AI 🧠

> **An Interactive Algorithm Visualisation and AI Tutoring Platform**

ALGOVISION.AI turns abstract data structures and algorithms into step-by-step visual experiences — with a built-in AI tutor you can ask questions at any point during a simulation.

---

## ✨ Features

- 🎞️ **Step-by-step animations** for 11 core DSA algorithms
- 🤖 **AI Tutor Panel** — pause any simulation and ask the AI a question, get a context-aware explanation
- ⚡ **Instant Step Explainer** — click "Explain This Step" for a sub-millisecond offline explanation
- 📊 **Complexity Analysis** — best, average, worst, and space complexity shown for every algorithm
- 💻 **Reference Code** — view implementations in JavaScript and Python side by side
- ✏️ **Custom Input** — provide your own arrays and graph edges to experiment with
- 🌐 **Publicly Deployed** — zero infrastructure cost using Vercel + Render

---

## 🧮 Algorithms Covered

| Algorithm | Category | Avg Time Complexity | Space |
|---|---|---|---|
| Binary Search | Searching | O(log n) | O(1) |
| Linear Search | Searching | O(n) | O(1) |
| Bubble Sort | Sorting | O(n²) | O(1) |
| Merge Sort | Sorting | O(n log n) | O(n) |
| Quick Sort | Sorting | O(n log n) | O(log n) |
| Stack | Data Structure | O(1) push/pop | O(n) |
| Queue | Data Structure | O(1) enqueue/dequeue | O(n) |
| Linked List | Data Structure | O(n) traversal | O(n) |
| Binary Tree | Data Structure | O(log n) insert | O(n) |
| Graph BFS | Graph | O(V + E) | O(V) |
| Graph DFS | Graph | O(V + E) | O(V) |

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Frontend Framework | React 19 |
| Build Tool | Vite 6 |
| Styling | Tailwind CSS |
| Animation | Framer Motion |
| Data Visualisation | D3.js |
| Backend | Node.js + Express.js |
| AI Model Host | Ollama (local LLM) |
| Frontend Deployment | Vercel |
| Backend Deployment | Render |

---

## 📁 Project Structure

```
ALGOVISION/
├── frontend/                  # React SPA
│   ├── src/
│   │   ├── components/        # UI components
│   │   │   ├── AITutorPanel.jsx
│   │   │   ├── AlgorithmSidebar.jsx
│   │   │   ├── CodePanel.jsx
│   │   │   ├── ComplexityPanel.jsx
│   │   │   ├── ControlBar.jsx
│   │   │   └── InputPanel.jsx
│   │   ├── visualizations/
│   │   │   └── VisualizerCanvas.jsx
│   │   ├── hooks/
│   │   │   └── useSimulation.js
│   │   ├── lib/
│   │   │   └── api.js
│   │   └── pages/
│   │       └── Dashboard.jsx
│   └── .env.example
├── backend/                   # Express API
│   ├── ai/
│   │   ├── ollamaClient.js    # Ollama integration + prompt builder
│   │   └── stepExplainer.js   # Instant offline explanations
│   ├── controllers/
│   ├── routes/
│   ├── server.js
│   └── .env.example
├── shared/
│   └── algorithms.js          # Pure simulation functions for all 11 algorithms
└── package.json               # Root monorepo config
```

---

## 🚀 Local Setup

### Prerequisites
- Node.js v20+
- [Ollama](https://ollama.com) installed and running locally

### 1. Clone the repository
```bash
git clone https://github.com/YOUR_USERNAME/ALGOVISION.git
cd ALGOVISION
```

### 2. Install dependencies
```bash
npm install
```

### 3. Set up environment variables
```bash
cp frontend/.env.example frontend/.env
cp backend/.env.example backend/.env
```

### 4. Pull an Ollama model
```bash
ollama pull deepseek-coder
# or
ollama pull codellama
```

### 5. Start the app
```bash
npm run dev
```

Frontend runs at `http://localhost:5173` and backend at `http://localhost:5001`.

---

## 🌍 Deployment

| Service | Platform | Config |
|---|---|---|
| Frontend | Vercel | Root directory: `frontend` |
| Backend | Render | Root directory: `backend`, see `render.yaml` |

### Environment Variables

**Backend** (`backend/.env`):
```
PORT=5001
CORS_ORIGIN=https://your-vercel-app.vercel.app
OLLAMA_BASE_URL=http://127.0.0.1:11434
OLLAMA_MODEL=deepseek-coder
```

**Frontend** (`frontend/.env`):
```
VITE_API_BASE_URL=https://your-render-backend.onrender.com/api
```

---

## 👨‍💻 Team

| Name | Enrollment No. |
|---|---|
| Kshitij Saxena | S24CSEU0050 |
| Harsh Khandelwal | S24CSEU1988 |
| Pratyaksh Manav | S24CSEU1976 |

**Mentor:** Prof. Dr. Aditya Upadhyay
**Institution:** School of Computer Science Engineering and Technology, Bennett University, Greater Noida

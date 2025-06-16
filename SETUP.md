## ⚙️ Getting Started

### ✅ Prerequisites

- Node.js ≥ 18
- Python ≥ 3.9
- Git
- pip, virtualenv

---

### 🔧 Setup Instructions

#### 1. Clone the repository

```bash
git clone https://github.com/yourusername/knowwhere-ai.git
cd knowwhere-ai
```

#### 2. Frontend Setup

```bash
cd frontend
npm install
npm run dev
```

#### 3. Backend Setup

```bash
cd backend
python -m venv venv
source venv/bin/activate    # or venv\Scripts\activate on Windows
pip install -r requirements.txt
uvicorn main:app --reload
```

#### 4. API Docs

Visit [http://localhost:8000/docs](http://localhost:8000/docs) for Swagger UI.

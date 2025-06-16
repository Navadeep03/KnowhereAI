# 🧠 KnowWhere.AI

**KnowWhere.AI** is a smart platform that combines intelligent document management with visual geo-intelligence. It enables enterprises to upload, classify, and search documents using AI while also mapping real-world events or structures through Apple Maps with rich metadata extracted from uploaded images.

---

## 🚀 Features

### 🔍 Intelligent Document Management
- Upload documents by selecting a high-level division (e.g., HR, Legal, Finance)
- OCR-based text extraction
- AI-powered classification of document type (e.g., NDA, Payslip, Agreement)
- Smart metadata enrichment:
  - Document type
  - Related entities (e.g., Employee, Vendor)
  - Section categorization (e.g., Internal, Employee)
  - Date, size, and extracted keywords
- Document ID generation: `Division_Category_SequentialID` (e.g., HR_LeavePolicy_001)
- Advanced search with filters:
  - By document name, ID, division, and date range
  - Natural language queries (e.g., "last year’s Pradeep’s payslips")
- Inline dropdown options: `View`, `Download`, `Metadata Details`, `Delete`
- Modal preview and document viewer

### 🗺️ Apple Maps GeoVision
- Apple-style map UI with real-time location tracking
- Upload image files (e.g., accident site, new building)
- System extracts:
  - Image metadata (date, time, location)
  - OCR-based contextual information (address, events)
- Smart marker/overlay placement on map
- Input methods:
  - Latitude & Longitude
  - PIN code or area name
  - Descriptive phrase (e.g., “jam near Ram Hospital”)
- Floor plan support: upload and validate layouts over location

## 🧱 Tech Stack

| Layer           | Tech                        |
|----------------|-----------------------------|
| Frontend        | React.js (Vite)             |
| Styling         | Tailwind CSS, Apple-style UI |
| Map Integration | Apple Maps JS SDK           |
| Backend         | FastAPI + Uvicorn           |
| OCR & AI        | Tesseract OCR, spaCy / custom ML |
| Storage         | Amazon S3 / Local FS        |
| Database        | PostgreSQL / SQLite         |
| Auth (optional) | JWT / OAuth2                |
| Dev Tools       | Prettier, ESLint, Swagger UI|

## 📁 Folder Structure

```
knowwhere-ai/
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   │   └── MapPage.jsx
│   │   └── styles/
│   │       └── MapPage.module.css
│   └── .env
├── backend/
│   ├── app/
│   │   ├── routers/
│   │   ├── services/
│   │   ├── models/
│   │   └── utils/
│   └── main.py
├── .gitignore
├── README.md
└── requirements.txt / package.json
```

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

## 🧠 Document ID Generation Format

```
{Division}_{AI Category}_{SequentialID}
Examples:
- HR_LeavePolicy_001
- Legal_NDA_002
```

## 🌐 Smart Search Examples

- “Pradeep’s payslips from 2023”
- “Agreements uploaded last month from Legal division”
- “Finance reports from January 2024”

## ✅ To-Do

- [ ] Finalize admin dashboard with document analytics
- [ ] Upload + validate floor plans for maps
- [ ] Dark mode toggle
- [ ] Export search results
- [ ] Role-based access controls

--

## 🙌 Contributing

1. Fork the project
2. Create a feature branch (`git checkout -b feature/my-feature`)
3. Commit changes (`git commit -m 'Add my feature'`)
4. Push to the branch (`git push origin feature/my-feature`)
5. Open a Pull Request

---

## 📬 Contact

- **Founder:** [Navadeep Vedantham](https://github.com/navadeep)
- **Email:** navadeep.v@payoda.com
- **Project URL:** [https://github.com/yourusername/knowwhere-ai](https://github.com/Navadeep03/KnowhereAI)

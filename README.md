# 🚀 AI Interview Prep

An AI-powered full-stack interview preparation platform built with **React**, **Node.js**, **MongoDB**, and **Google Gemini AI**. It analyzes a candidate's resume alongside a target job description to generate a personalized interview report, match score, tailored questions, skill gap analysis, and a multi-day preparation roadmap.

---

## ✨ Key Features

- **Smart Resume & JD Analysis:** Upload a PDF resume or paste text alongside any job description for automated AI evaluation.
- **Match Score & Skill Gap Insights:** Instantly calculates how well your profile aligns with the role and highlights missing skills to work on.
- **Tailored Question Bank:** Generates categorized technical and behavioral interview questions customized to your background and target job.
- **Multi-Day Preparation Roadmap:** Builds a structured, step-by-step study schedule to guide your prep before interview day.
- **Downloadable PDF Reports:** Export your complete interview preparation plan as a clean, formatted PDF.
- **Secure User Authentication:** Full user registration and login system powered by JWT and password hashing.

---

## 🛠️ Tech Stack

### Frontend
- **Framework:** React (bootstrapped with Vite)
- **Styling:** CSS
- **State Management:** React Context API (`AuthContext`, `InterviewContext`)

### Backend
- **Runtime & Framework:** Node.js, Express.js
- **Database:** MongoDB (Mongoose)
- **AI Engine:** Google Gemini (`@google/genai` SDK)
- **File Handling:** `multer` (file uploads) & `pdf-parse` (resume text extraction)
- **Authentication:** `jsonwebtoken` (JWT) & `bcryptjs`

---

## 📂 Project Structure

```text
AI-interview-prep/
├── Backend/
│   ├── controllers/       # Auth & interview report request handlers
│   ├── middlewares/       # JWT verification & Multer file upload middleware
│   ├── models/            # Mongoose schemas (User & InterviewReport)
│   ├── routes/            # REST API endpoints (/auth, /interview)
│   ├── services/          # Google Gemini AI prompt & PDF generation logic
│   ├── server.js          # Express app entry point
│   └── package.json
└── Frontend/
    ├── public/
    ├── src/
    │   ├── context/       # Global state (AuthProvider, InterviewProvider)
    │   └── ...            # Pages, components, hooks, and SCSS styles
    ├── index.html
    └── package.json
```

---

## ⚙️ Getting Started (Local Setup)

### 1. Clone the Repository
```bash
git clone https://github.com
cd AI-interview-prep
```

### 2. Backend Configuration
Navigate to the `Backend` folder and install dependencies:
```bash
cd Backend
npm install
```

Create a `.env` file inside the `Backend` directory and configure the following environment variables:
```env
PORT=3000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key
GEMINI_API_KEY=your_google_gemini_api_key
```

Start the backend server:
```bash
npm start
```

### 3. Frontend Configuration
Open a new terminal window, navigate to the `Frontend` folder, and install dependencies:
```bash
cd Frontend
npm install
npm run dev
```

Open the local URL shown in your terminal (typically `http://localhost:5173`) to use the app.

---


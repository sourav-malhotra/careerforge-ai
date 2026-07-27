# CareerForge AI

**A Production-Ready Full Stack Gen AI Job Preparation Platform**

CareerForge AI is a full-stack web application that helps job seekers prepare smarter. Upload your resume, paste a target job description, and get instant AI-powered skill-gap analysis, personalized interview questions, a tailored prep roadmap, and an ATS-optimized resume — generated as a downloadable PDF.

---

## ✨ Features

- 🔐 **Secure Authentication** — JWT-based registration/login with token blacklisting for proper logout handling
- 📄 **Resume & JD Processing** — Upload a resume and paste any job description for instant analysis
- 🤖 **AI-Powered Skill Gap Analysis** — Google Gemini AI compares your resume against the job description and identifies missing skills
- 🎯 **AI-Generated Interview Questions** — Get tailored technical and behavioral interview questions based on the specific role
- 🗺️ **Personalized Prep Roadmap** — Receive a structured plan to close your skill gaps before the interview
- 📑 **ATS-Optimized Resume Generation** — Puppeteer dynamically renders AI-generated content into a clean, ATS-friendly PDF resume

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Frontend | React.js, Vite |
| Backend | Node.js, Express.js |
| Database | MongoDB Atlas |
| AI | Google Gemini API |
| PDF Generation | Puppeteer |
| Authentication | JWT (JSON Web Tokens) |

---

## 🏗️ Architecture

The project follows a modern full-stack architecture with a clear separation of concerns:

- **Service layer** for business logic, kept separate from route handlers
- **Context-based state management** on the frontend for auth and app-wide state
- **Custom React hooks** for reusable logic (API calls, form handling, etc.)
- **Centralized error handling** across both frontend and backend
- **Token blacklisting** for secure, stateless-friendly logout

```
careerforge-ai/
├── Backend/          # Node.js + Express API, Gemini integration, PDF generation
└── Frontend/          # React + Vite client application
```

---

## 🚀 Getting Started

### Prerequisites

- Node.js (v18+ recommended)
- MongoDB Atlas account (or local MongoDB instance)
- Google Gemini API key

### 1. Clone the repository

```bash
git clone https://github.com/sourav-malhotra/careerforge-ai.git
cd careerforge-ai
```

### 2. Backend Setup

```bash
cd Backend
npm install
```

Create a `.env` file in the `Backend` directory:

```env
PORT=5000
MONGO_URI=your_mongodb_atlas_connection_string
JWT_SECRET=your_jwt_secret
GEMINI_API_KEY=your_gemini_api_key
```

Start the backend server:

```bash
npm start
```

### 3. Frontend Setup

```bash
cd ../Frontend
npm install
```

Create a `.env` file in the `Frontend` directory:

```env
VITE_API_BASE_URL=http://localhost:5000
```

Start the frontend dev server:

```bash
npm run dev
```

### 4. Open the app

Visit `http://localhost:5173` (or the port Vite assigns) in your browser.

---

## 📋 How It Works

1. **Sign up / Log in** — Create a secure account protected by JWT authentication
2. **Upload your resume** — Provide your resume and paste the job description you're targeting
3. **Get your analysis** — Gemini AI evaluates the gap between your current skills and the role's requirements
4. **Prepare with AI** — Review AI-generated interview questions and a personalized roadmap to close skill gaps
5. **Download your resume** — Generate and download an ATS-optimized PDF resume tailored to the job

---

## 🗺️ Roadmap / Future Improvements

- [ ] Support for multiple resume templates
- [ ] Mock interview mode with AI feedback on answers
- [ ] Resume version history and comparison
- [ ] Multi-language support
- [ ] Integration with job boards for auto-fetching JDs

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome. Feel free to open an issue or submit a pull request.

---

## 📄 License

This project is licensed under the MIT License.

---

## 👤 Author

**Sourav Malhotra**
Final-year B.Tech Software Engineering student, Delhi Technological University (DTU)

- GitHub: [@sourav-malhotra](https://github.com/sourav-malhotra)

---

⭐ If you find this project useful, consider giving it a star!

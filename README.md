# CareerForge AI

A full-stack AI-powered interview preparation platform that helps users practice and improve their interview skills with realistic mock interviews, AI-generated questions, and detailed feedback.

## 🚀 Features

- **AI-Powered Mock Interviews** - Practice with AI-generated questions tailored to your role and experience level
- **Real-time Feedback** - Get instant analysis and scoring on your responses
- **Interview Reports** - Detailed performance reports with strengths and areas for improvement
- **Authentication** - Secure JWT-based auth with protected routes
- **Resume Upload** - Parse and analyze resumes for personalized interview prep
- **Modern UI** - Clean, responsive interface built with React 19 and SCSS

## 🛠 Tech Stack

### Backend
- **Runtime**: Node.js with Express 5
- **Database**: MongoDB with Mongoose
- **Authentication**: JWT + bcryptjs
- **AI Integration**: Google GenAI (@google/genai)
- **File Processing**: Multer + pdf-parse
- **Validation**: Zod
- **Other**: Puppeteer, cookie-parser, cors, dotenv

### Frontend
- **Framework**: React 19 with Vite 7
- **Routing**: React Router 7
- **Styling**: SCSS/Sass
- **HTTP Client**: Axios
- **Linting**: ESLint 9 with React hooks plugin

## 📁 Project Structure

```
careerforge-ai/
├── Backend/
│   ├── src/
│   │   ├── config/         # Database configuration
│   │   ├── controllers/    # Request handlers
│   │   ├── middlewares/    # Auth, file upload middlewares
│   │   ├── models/         # Mongoose models (User, InterviewReport, Blacklist)
│   │   ├── routes/         # API routes (auth, interview)
│   │   ├── services/       # Business logic (AI service)
│   │   ├── app.js          # Express app setup
│   │   └── server.js       # Entry point
│   ├── package.json
│   └── .gitignore
├── Frontend/
│   ├── src/
│   │   ├── features/
│   │   │   ├── auth/       # Auth context, hooks, pages, components
│   │   │   └── interview/  # Interview context, hooks, pages, styles
│   │   ├── app.routes.jsx  # Route definitions
│   │   ├── App.jsx         # Root component
│   │   ├── main.jsx        # Entry point
│   │   └── style.scss      # Global styles
│   ├── public/
│   ├── package.json
│   ├── vite.config.js
│   └── .gitignore
└── README.md
```

## ⚙️ Getting Started

### Prerequisites
- Node.js 18+
- MongoDB instance (local or cloud)
- Google GenAI API key

### Backend Setup

```bash
cd Backend
npm install

# Create .env file with:
# PORT=5000
# MONGODB_URI=your_mongodb_connection_string
# JWT_SECRET=your_jwt_secret
# GOOGLE_GENAI_API_KEY=your_genai_key

npm run dev
```

Server runs on `http://localhost:5000`

### Frontend Setup

```bash
cd Frontend
npm install
npm run dev
```

App runs on `http://localhost:5173`

## 🔐 Environment Variables

### Backend (.env)
| Variable | Description |
|----------|-------------|
| `PORT` | Server port (default: 5000) |
| `MONGODB_URI` | MongoDB connection string |
| `JWT_SECRET` | Secret for JWT signing |
| `GOOGLE_GENAI_API_KEY` | Google GenAI API key |

## 📡 API Endpoints

### Authentication
- `POST /api/auth/register` - Register new user
- `POST /api/auth/login` - Login user
- `POST /api/auth/logout` - Logout user
- `GET /api/auth/me` - Get current user

### Interviews
- `POST /api/interviews` - Create new interview session
- `GET /api/interviews` - Get user's interviews
- `GET /api/interviews/:id` - Get interview details
- `POST /api/interviews/:id/respond` - Submit response
- `GET /api/interviews/:id/report` - Get interview report

## 🎯 Usage

1. **Register/Login** - Create an account or sign in
2. **Start Interview** - Choose role, experience level, and interview type
3. **Answer Questions** - Respond to AI-generated questions
4. **Get Feedback** - Receive detailed analysis and scores
5. **Review Reports** - Track progress over time

## 📝 Scripts

### Backend
```bash
npm run dev      # Start development server with nodemon
```

### Frontend
```bash
npm run dev      # Start Vite dev server
npm run build    # Build for production
npm run lint     # Run ESLint
npm run preview  # Preview production build
```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit changes (`git commit -m 'Add amazing feature'`)
4. Push to branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the ISC License.

## 👨‍💻 Author

**Sourav Malhotra**
- GitHub: [@sourav-malhotra](https://github.com/sourav-malhotra)

---

Built with ❤️ for interview preparation
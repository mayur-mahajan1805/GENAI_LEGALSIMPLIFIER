# LegalSimplify

LegalSimplify is an AI-powered web application that simplifies complex legal documents by translating legal jargon into plain, understandable language. Built as a full-stack application for a startathon, it helps users make sense of contracts, agreements, and other legal texts without needing extensive legal knowledge.

## 🚀 Features

- **Document Simplification**: Upload PDF documents and get simplified versions in plain language
- **Text-to-Speech**: Convert simplified text into audio for easy listening
- **Multi-language Translation**: Translate legal documents into different languages
- **User Authentication**: Secure user registration and login system
- **Responsive Design**: Modern, mobile-friendly interface built with React and Tailwind CSS
- **Dark Mode Support**: Toggle between light and dark themes
- **File Upload**: Support for PDF file uploads with cloud storage integration

## 🛠️ Tech Stack

### Frontend
- **React 19** - Modern JavaScript library for building user interfaces
- **Vite** - Fast build tool and development server
- **Tailwind CSS** - Utility-first CSS framework
- **Framer Motion** - Animation library for React
- **React Router** - Declarative routing for React
- **Axios** - HTTP client for API requests
- **Lucide React** - Beautiful icon library

### Backend
- **Node.js** - JavaScript runtime
- **Express.js** - Web application framework
- **MongoDB** - NoSQL database with Mongoose ODM
- **JWT** - JSON Web Tokens for authentication
- **bcrypt** - Password hashing
- **Multer** - Middleware for handling file uploads
- **Cloudinary** - Cloud storage for uploaded files

### AI & External Services
- **OpenAI API** - For document simplification
- **Google Generative AI** - Alternative AI processing
- **Google Cloud Text-to-Speech** - Audio generation
- **Google Translate API** - Language translation

## 📋 Prerequisites

Before running this application, make sure you have the following installed:

- **Node.js** (v16 or higher)
- **npm** or **yarn**
- **MongoDB** (local or cloud instance)
- **Git**

## 🔧 Installation

1. **Clone the repository**
   ```bash
   git clone <your-github-repo-url>
   cd LegalSimplifier
   ```

2. **Backend Setup**
   ```bash
   cd GENAI_BACKEND
   npm install
   ```

3. **Frontend Setup**
   ```bash
   cd ../GENAI_Frontend
   npm install
   ```

## ⚙️ Environment Configuration

### Backend Environment Variables

Create a `.env` file in the `GENAI_BACKEND` directory with the following variables:

```env
PORT=8000
MONGODB_URI=mongodb://localhost:27017/legalsimplify
CORS_ORIGIN=http://localhost:5173

# JWT Configuration
ACCESS_TOKEN_SECRET=your_access_token_secret
ACCESS_TOKEN_EXPIRY=1d
REFRESH_TOKEN_SECRET=your_refresh_token_secret
REFRESH_TOKEN_EXPIRY=10d

# OpenAI API
OPENAI_API_KEY=your_openai_api_key

# Google Cloud
GOOGLE_GENERATIVE_AI_API_KEY=your_google_ai_api_key
GOOGLE_CLOUD_PROJECT_ID=your_project_id
GOOGLE_CLOUD_PRIVATE_KEY=your_private_key
GOOGLE_CLOUD_CLIENT_EMAIL=your_client_email

# Cloudinary
CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret
```

### Frontend Environment Variables

Create a `.env` file in the `GENAI_Frontend` directory:

```env
VITE_API_BASE_URL=http://localhost:8000/api/v1
```

## 🚀 Running the Application

1. **Start the Backend Server**
   ```bash
   cd GENAI_BACKEND
   npm run dev
   ```
   The backend will run on `http://localhost:8000`

2. **Start the Frontend Development Server**
   ```bash
   cd GENAI_Frontend
   npm run dev
   ```
   The frontend will run on `http://localhost:5173`

3. **Open your browser** and navigate to `http://localhost:5173`

## 📡 API Endpoints

### Authentication
- `POST /api/v1/user/register` - User registration
- `POST /api/v1/user/login` - User login
- `POST /api/v1/user/logout` - User logout
- `GET /api/v1/user/getCurrent-user` - Get current user info

### Document Processing
- `POST /api/v1/simplify/generate-simplyfy` - Simplify PDF document
- `POST /api/v1/translate/translate` - Translate text
- `POST /api/v1/voice/generateSpeech` - Generate speech from text

## 🏗️ Project Structure

```
LegalSimplifier/
├── GENAI_BACKEND/
│   ├── src/
│   │   ├── controllers/     # Request handlers
│   │   ├── middlewares/     # Custom middleware
│   │   ├── models/         # Database models
│   │   ├── routes/         # API routes
│   │   ├── utils/          # Utility functions
│   │   ├── app.js          # Express app setup
│   │   └── index.js        # Server entry point
│   ├── public/             # Static files
│   └── package.json
└── GENAI_Frontend/
    ├── src/
    │   ├── components/     # React components
    │   ├── assets/         # Static assets
    │   └── main.jsx        # App entry point
    ├── public/             # Public assets
    └── package.json
```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the ISC License - see the package.json files for details.

## 🙏 Acknowledgments

- Built for a startathon competition
- Powered by OpenAI, Google Cloud AI, and other modern AI services
- Icons provided by Lucide React
- UI components inspired by modern design systems

## 📞 Support

If you have any questions or need help, please open an issue in the GitHub repository.
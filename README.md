<div align="center">
  <img src="https://img.shields.io/badge/CodeTogether-Interview%20Platform-6366f1?style=for-the-badge&logo=github&logoColor=white" alt="CodeTogether Badge">
  <h1 align="center">🚀 CodeTogether - Interview Platform 🚀</h1>
  
  <p align="center">
    A full-stack real-time coding interview platform built with modern web technologies
    <br />
    <br />
    <a href="https://github.com/bouzayenilyes/code-together"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    <a href="https://github.com/bouzayenilyes/code-together/issues">Report Bug</a>
    ·
    <a href="https://github.com/bouzayenilyes/code-together/issues">Request Feature</a>
  </p>
</div>

<!-- Badges -->
<p align="center">
  <a href="https://github.com/bouzayenilyes/code-together/actions/workflows/ci.yml">
    <img src="https://img.shields.io/github/actions/workflow/status/bouzayenilyes/code-together/ci.yml?branch=main&style=for-the-badge" alt="CI">
  </a>
  <a href="https://github.com/bouzayenilyes/code-together/pulls">
    <img src="https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=for-the-badge" alt="PRs Welcome">
  </a>
  <a href="https://github.com/bouzayenilyes/code-together/blob/main/LICENSE">
    <img src="https://img.shields.io/github/license/bouzayenilyes/code-together?style=for-the-badge" alt="License">
  </a>
  <a href="https://github.com/bouzayenilyes/code-together/stargazers">
    <img src="https://img.shields.io/github/stars/bouzayenilyes/code-together?style=for-the-badge" alt="GitHub stars">
  </a>
  <a href="https://github.com/bouzayenilyes/code-together/network/members">
    <img src="https://img.shields.io/github/forks/bouzayenilyes/code-together?style=for-the-badge" alt="GitHub forks">
  </a>
</p>

---

## 📖 Table of Contents

- [About the Project](#about-the-project)
- [Key Features](#key-features)
- [Tech Stack](#tech-stack)
- [Architecture](#architecture)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Environment Variables](#environment-variables)
- [Project Structure](#project-structure)
- [Development Workflow](#development-workflow)
- [Deployment](#deployment)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

---

## 🎯 About the Project

CodeTogether is a comprehensive real-time coding interview platform designed to streamline the technical interview process. Built with modern web technologies, this platform provides an immersive interview experience with real-time collaboration, code execution, and video capabilities.

The project is maintained by **Bouzayeni Ilyes** and demonstrates expertise in full-stack development, real-time applications, and modern JavaScript/TypeScript ecosystems.

---

## ✨ Key Features

### 🧑‍💻 Development Environment
- **VSCode-Powered Code Editor**: Full-featured code editing with syntax highlighting, autocompletion, and real-time collaboration
- **Multi-language Support**: Execute code in multiple programming languages with isolated environments
- **Real-time Collaboration**: Live code sharing and simultaneous editing between interviewers and candidates
- **Code Execution**: Secure code execution in isolated environments with instant feedback

### 🎥 Communication & Collaboration
- **1-on-1 Video Interview Rooms**: High-quality video conferencing with Stream Video SDK
- **Real-time Chat Messaging**: Integrated chat system with file sharing capabilities
- **Screen Sharing**: Share your screen during technical explanations
- **Recording**: Record interview sessions for later review
- **Audio Controls**: Individual mic and camera toggle with permission management

### 📊 Analytics & Feedback
- **Live Dashboard**: Real-time statistics and interview metrics
- **Auto Feedback**: Automated success/failure feedback based on test cases
- **Confetti Celebrations**: Visual feedback for successful completions
- **Notification System**: Real-time notifications for all events
- **Performance Metrics**: Track coding speed, accuracy, and problem-solving patterns

### 🔒 Security & Reliability
- **Authentication**: Secure user authentication with Clerk
- **Room Locking**: Ensures only 2 participants per interview room
- **Data Encryption**: End-to-end encryption for all communications
- **Isolated Execution**: Code runs in secure, sandboxed environments
- **Rate Limiting**: API protection against abuse and DDoS attacks

### 🚀 Developer Experience
- **Type Safety**: Full TypeScript support across the application
- **Hot Module Replacement**: Instant development feedback
- **Automated Testing**: Comprehensive test suite with Jest and React Testing Library
- **Code Quality**: ESLint, Prettier, and automated code reviews
- **CI/CD**: Automated testing and deployment pipeline

---

## 🛠️ Tech Stack

### Frontend
- **Framework**: React 19 with TypeScript
- **Build Tool**: Vite for lightning-fast development and builds
- **Styling**: Tailwind CSS with DaisyUI components
- **State Management**: React Query for server state and React Context for client state
- **Routing**: React Router v7 for seamless navigation
- **UI Components**: Lucide React for icons and custom components
- **Real-time Updates**: Stream Chat SDK for messaging and collaboration

### Backend
- **Runtime**: Node.js with ES Modules
- **Framework**: Express.js for REST API
- **Database**: MongoDB with Mongoose ODM
- **Authentication**: Clerk for secure user management
- **Real-time Communication**: Stream Chat and Video SDKs
- **Background Processing**: Inngest for reliable async task execution
- **Security**: CORS, helmet, and rate limiting middleware

### Development & DevOps
- **Code Quality**: ESLint, Prettier, TypeScript
- **Testing**: Jest, React Testing Library, Vitest
- **Package Management**: npm with workspaces
- **Deployment**: Sevalla (free-tier friendly)
- **Version Control**: Git with conventional commits

---

## 🏗️ Architecture

```
┌─────────────────────────────────────────────────────────────────┐
│                         Frontend (React)                         │
│  ┌─────────────┐  ┌─────────────┐  ┌─────────────┐  ┌─────────┐  │
│  │  Dashboard  │  │  Code Editor │  │  Video Call │  │  Chat   │  │
│  └─────────────┘  └─────────────┘  └─────────────┘  └─────────┘  │
└─────────────────────────────────────────────────────────────────┘
                                │
                                ▼
┌─────────────────────────────────────────────────────────────────┐
│                         Backend (Node.js)                        │
│  ┌─────────────┐  ┌─────────────┐  ┌─────────────┐  ┌─────────┐  │
│  │   Auth API  │  │   Chat API  │  │   Video API │  │  Code   │  │
│  │  (Clerk)    │  │  (Stream)   │  │  (Stream)   │  │ Execute │  │
│  └─────────────┘  └─────────────┘  └─────────────┘  │  API    │  │
│                                                  └─────────┘  │
│  ┌─────────────┐  ┌─────────────┐  ┌─────────────┐             │
│  │   Sessions  │  │   Problems  │  │   Analytics │             │
│  │   (MongoDB) │  │   (MongoDB) │  │   (MongoDB) │             │
│  └─────────────┘  └─────────────┘  └─────────────┘             │
└─────────────────────────────────────────────────────────────────┘
                                │
                                ▼
┌─────────────────────────────────────────────────────────────────┐
│                        External Services                         │
│  ┌─────────────┐  ┌─────────────┐  ┌─────────────┐             │
│  │   Clerk     │  │   Stream    │  │   Inngest   │             │
│  │  (Auth)     │  │ (Chat/Video)│  │ (Background │             │
│  └─────────────┘  └─────────────┘  │   Tasks)    │             │
│  ┌─────────────┐  ┌─────────────┐  └─────────────┘             │
│  │   MongoDB   │  │   Piston    │                               │
│  │   (Database)│  │(Code Exec)  │                               │
│  └─────────────┘  └─────────────┘                               │
└─────────────────────────────────────────────────────────────────┘
```

---

## 🚀 Getting Started

### Prerequisites

Before you begin, ensure you have the following installed:

- **Node.js**: v18.x or higher
- **npm**: v8.x or higher
- **Git**: For version control
- **MongoDB**: Local or cloud instance
- **Clerk Account**: For authentication
- **Stream Account**: For real-time communication

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/bouzayenilyes/code-together.git
   cd code-together
   ```

2. **Install dependencies**
   ```bash
   # Install root dependencies
   npm install
   
   # Install backend dependencies
   cd backend
   npm install
   
   # Install frontend dependencies
   cd ../frontend
   npm install
   
   # Return to root
   cd ..
   ```

3. **Set up environment variables**
   ```bash
   # Copy environment files
   cp backend/.env.example backend/.env
   cp frontend/.env.example frontend/.env
   ```

### Environment Variables

#### Backend (`.env`)
```env
# Server Configuration
PORT=3000
NODE_ENV=development
CLIENT_URL=http://localhost:5173

# Database
DB_URL=your_mongodb_connection_string

# Authentication (Clerk)
CLERK_PUBLISHABLE_KEY=your_clerk_publishable_key
CLERK_SECRET_KEY=your_clerk_secret_key

# Real-time Communication (Stream)
STREAM_API_KEY=your_stream_api_key
STREAM_API_SECRET=your_stream_api_secret

# Background Processing (Inngest)
INNGEST_EVENT_KEY=your_inngest_event_key
INNGEST_SIGNING_KEY=your_inngest_signing_key
```

#### Frontend (`.env`)
```env
# API Configuration
VITE_API_URL=http://localhost:3000/api
VITE_CLERK_PUBLISHABLE_KEY=your_clerk_publishable_key
VITE_STREAM_API_KEY=your_stream_api_key
```

---

## 📁 Project Structure

```
code-together/
├── backend/                 # Node.js/Express backend
│   ├── src/
│   │   ├── controllers/     # Request handlers
│   │   ├── lib/            # Utility libraries
│   │   ├── middleware/     # Express middleware
│   │   ├── models/         # Database models
│   │   ├── routes/         # API routes
│   │   └── server.js       # Main server file
│   ├── .env.example        # Environment variables template
│   └── package.json        # Backend dependencies
├── frontend/               # React/Vite frontend
│   ├── src/
│   │   ├── api/            # API client functions
│   │   ├── components/     # React components
│   │   ├── hooks/          # Custom React hooks
│   │   ├── lib/            # Utility libraries
│   │   ├── pages/          # Page components
│   │   └── data/           # Static data
│   ├── public/             # Static assets
│   ├── .env.example        # Environment variables template
│   └── package.json        # Frontend dependencies
├── .gitignore              # Git ignore rules
└── package.json            # Root package.json
```

---

## 🔄 Development Workflow

### Running the Application

1. **Start the Backend**
   ```bash
   cd backend
   npm run dev
   ```
   The backend will start on `http://localhost:3000`

2. **Start the Frontend**
   ```bash
   cd frontend
   npm run dev
   ```
   The frontend will start on `http://localhost:5173`

3. **Access the Application**
   Open your browser and navigate to `http://localhost:5173`

### Available Scripts

```bash
# Root level
npm run build    # Build the entire application
npm run start    # Start the production backend

# Backend
npm run dev      # Start development server with nodemon
npm start        # Start production server

# Frontend
npm run dev      # Start development server
npm run build    # Build for production
npm run preview  # Preview production build
npm run lint     # Run ESLint
```

### Development Guidelines

- Follow the [Conventional Commits](https://www.conventionalcommits.org/) format
- Write tests for new features and bug fixes
- Use TypeScript for type safety
- Follow the existing code style and patterns
- Run linting and type checking before committing

---

## 🚀 Deployment

### Production Build

```bash
# Build the entire application
npm run build

# Start the production backend
npm start
```

### Deployment Options

1. **Sevalla (Recommended)**
   - Free-tier friendly platform
   - Automatic SSL certificates
   - Easy deployment with GitHub integration

2. **Vercel + Railway**
   - Frontend: Vercel
   - Backend: Railway
   - Database: MongoDB Atlas

3. **Docker Deployment**
   ```bash
   # Build and run with Docker Compose
   docker-compose up --build
   ```

### Environment Setup for Production

1. **Update Environment Variables**
   ```env
   # Backend
   NODE_ENV=production
   CLIENT_URL=https://your-domain.com
   
   # Frontend
   VITE_API_URL=https://api.your-domain.com
   ```

2. **Configure Production Services**
   - Set up production MongoDB instance
   - Configure Clerk production settings
   - Set up Stream production credentials
   - Configure Inngest production environment

---

## 🤝 Contributing

Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

### How to Contribute

1. **Fork the Project**
   ```bash
   git clone https://github.com/bouzayenilyes/code-together.git
   cd code-together
   ```

2. **Create your Feature Branch** (`git checkout -b feature/AmazingFeature`)

3. **Make Changes** and commit them (`git commit -m 'feat: Add some AmazingFeature'`)

4. **Push to the Branch** (`git push origin feature/AmazingFeature`)

5. **Open a Pull Request**

### Development Guidelines

- Follow the existing code style and patterns
- Write comprehensive tests for new features
- Update documentation as needed
- Ensure all tests pass before submitting
- Use conventional commit messages

### Code of Conduct

Please read and follow our [Code of Conduct](CODE_OF_CONDUCT.md) to ensure a positive environment for all contributors.

---

## 📄 License

Distributed under the ISC License. See `LICENSE` for more information.

---

## 📞 Contact

**Bouzayen Ilyes** - [@bouzayenilyes](https://github.com/bouzayenilyes) - bouzayenilyes@example.com

Project Link: [https://github.com/bouzayenilyes/code-together](https://github.com/bouzayenilyes/code-together)

---

<div align="center">
  <p>Made with ❤️ by <a href="https://github.com/bouzayenilyes">Bouzayen Ilyes</a></p>
  
  ![Visitor Count](https://komarev.com/ghpvc/?username=bouzayenilyes&repo=code-together&style=for-the-badge)
</div>

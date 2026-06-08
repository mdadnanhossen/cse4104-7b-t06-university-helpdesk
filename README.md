# AI-Powered University Helpdesk

**Team:** CSE4104-7B-T06 | **Section:** 7B | **Course:** CSE 4104

## Team Members
| Name | ID | Role |
|------|----|------|
| Md Adnan Hossen | 1135 | Team Leader / Frontend + AI |
| Jaber | 1105 | Backend Developer |
| Sk Mirazur Rahman Nayon | 1131 | Database + Testing |
| Sazid Hasan | 1122 | Documentation + Deployment |

## Project Description
An AI-powered university helpdesk where students can ask queries about admission, courses, fees, and schedules. Google Gemini AI provides instant intelligent responses 24/7.

## Features
- JWT Authentication (Student & Admin)
- AI Chat powered by Google Gemini
- Conversation History
- Admin Panel
- Analytics Dashboard

## Tech Stack
| Layer | Technology |
|-------|-----------|
| Frontend | React.js, Tailwind CSS |
| Backend | Node.js, Express.js |
| Database | MongoDB Atlas |
| AI | Google Gemini API |
| Deployment | Vercel + Render |

# 🎓 AI-Powered University Helpdesk

> An intelligent, always-available university helpdesk system powered by Google Gemini AI. Students can ask queries about admission, courses, fees, and schedules and receive instant, accurate responses 24/7.

---

## 👥 Team Information

| Field | Details |
|-------|---------|
| **Team Name** | CSE4104-7B-T06 |
| **Section** | 7B |
| **Course** | CSE 4104 — Software Development III |
| **University** | Northern University of Business and Technology, Khulna |

| No. | Name | Student ID | Role |
|-----|------|-----------|------|
| 01 | Md Adnan Hossen | 11230121135 | Team Leader / Frontend + AI Integration |
| 02 | Jaber | 11230121105 | Backend Developer |
| 03 | Sk Mirazur Rahman Nayon | 11230121131 | Database + Testing |
| 04 | Sazid Hasan | 11230121122 | Documentation + Deployment |

---

## 📌 Project Overview

AI-Powered University Helpdesk is a full-stack web application designed to provide university students with instant, intelligent responses to their academic and administrative queries. The system integrates **Google Gemini AI** to understand and respond to natural language questions related to:

- Admission procedures
- Course registration
- Fee payments
- Examination schedules
- Campus facilities

The platform is accessible **24/7** and includes a dedicated admin panel for university staff to monitor and manage student queries.

---

## ⚠️ Problem Statement

University students frequently face difficulties in obtaining timely and accurate information regarding academic and administrative matters. Existing manual helpdesk systems are only available during office hours, cannot handle large volumes of simultaneous queries, and existing solutions like static FAQ pages cannot understand natural language. There is a clear need for an intelligent, always-available AI-powered system that provides instant, accurate responses.

---

## 🎯 Objectives

- Build an AI-powered university helpdesk web application for students and admin staff.
- Integrate Google Gemini AI to provide instant, intelligent responses to student queries.
- Implement secure user authentication for students and admin using JWT.
- Store all conversation history in MongoDB for future reference and admin review.
- Build a dedicated admin panel to monitor, manage, and resolve student queries.
- Provide an analytics dashboard displaying helpdesk usage statistics.
- Deploy the complete system online for public access.

---

## ✨ Features

### 🔐 Authentication
- Student and admin registration and login
- Secure password hashing using bcrypt
- JWT-based role management

### 🤖 AI Chat Interface
- Natural language query submission
- Google Gemini AI generates instant responses
- Conversation context maintained throughout session

### 📜 Conversation History
- All chat sessions saved per user
- Students can review previous conversations

### 🛠️ Admin Panel
- View all student conversations
- Mark queries as resolved or open
- Manage student accounts

### 📊 Analytics Dashboard
- Total queries, resolved rate, active users
- Visual charts for helpdesk usage trends

---

## 🛠️ Technology Stack

| Layer | Technology |
|-------|-----------|
| **Frontend** | React.js, Tailwind CSS |
| **Backend** | Node.js, Express.js |
| **Database** | MongoDB (MongoDB Atlas) |
| **AI Integration** | Google Gemini API |
| **Authentication** | JWT, bcrypt |
| **Frontend Deployment** | Vercel |
| **Backend Deployment** | Render |
| **Version Control** | GitHub |
| **API Testing** | Postman |
| **UI Design** | Figma |

---

## 📁 Repository Structure

```
ai-university-helpdesk/
├── frontend/
│   ├── src/
│   │   ├── pages/
│   │   │   ├── LoginPage.jsx
│   │   │   ├── RegisterPage.jsx
│   │   │   ├── ChatPage.jsx
│   │   │   ├── HistoryPage.jsx
│   │   │   ├── DashboardPage.jsx
│   │   │   └── AdminPage.jsx
│   │   ├── components/
│   │   │   ├── auth/
│   │   │   ├── chat/
│   │   │   ├── admin/
│   │   │   └── dashboard/
│   │   ├── context/
│   │   │   └── AuthContext.jsx
│   │   ├── hooks/
│   │   │   └── useChat.js
│   │   └── utils/
│   │       └── api.js
│   ├── package.json
│   └── vite.config.js
├── backend/
│   ├── server.js
│   ├── config/
│   │   └── db.js
│   ├── models/
│   │   ├── User.js
│   │   └── Conversation.js
│   ├── controllers/
│   │   ├── authController.js
│   │   ├── chatController.js
│   │   └── adminController.js
│   ├── routes/
│   │   ├── authRoutes.js
│   │   ├── chatRoutes.js
│   │   └── adminRoutes.js
│   └── middleware/
│       └── authMiddleware.js
├── README.md
└── .gitignore
```

---

## 🚀 Installation & Setup

### Prerequisites
- Node.js v18+
- MongoDB Atlas account
- Google Gemini API key

### Backend Setup
```bash
cd backend
npm install
cp .env.example .env
# Fill in your .env values
npm run dev
```

### Frontend Setup
```bash
cd frontend
npm install
cp .env.example .env
npm run dev
```

### Environment Variables

**Backend `.env`:**
```
PORT=5000
MONGO_URI=your_mongodb_atlas_connection_string
JWT_SECRET=your_jwt_secret_key
GEMINI_API_KEY=your_gemini_api_key
```

**Frontend `.env`:**
```
VITE_API_URL=http://localhost:5000/api
```

---

## 🌐 API Endpoints

| Method | Endpoint | Description | Access |
|--------|---------|-------------|--------|
| POST | `/api/auth/register` | Register new student | Public |
| POST | `/api/auth/login` | Login user | Public |
| POST | `/api/chat/send` | Send message to AI | Student |
| GET | `/api/chat/history` | Get conversation list | Student |
| GET | `/api/chat/:id` | Get single conversation | Student |
| GET | `/api/admin/conversations` | Get all conversations | Admin |
| PATCH | `/api/admin/conversations/:id` | Update query status | Admin |
| GET | `/api/admin/stats` | Get dashboard statistics | Admin |

---

## 👤 User Roles

| Role | Permissions |
|------|------------|
| **Student** | Register, Login, Send queries, View own history, Start new conversations |
| **Admin** | Login, View all conversations, Update query status, View analytics, Manage users |

---

## 🔗 Live Demo

| Service | URL |
|---------|-----|
| Frontend | *(Vercel link — after deployment)* |
| Backend | *(Render link — after deployment)* |

---

## 📅 Development Timeline

| Week | Phase | Deliverable |
|------|-------|------------|
| 1 | Team Formation | Team info, GitHub setup |
| 2 | Proposal | Project proposal document |
| 3 | SRS | Software Requirement Specification |
| 4 | System Design | Architecture, ER diagram, API structure |
| 5 | UI/UX Design | Figma wireframes |
| 6 | Backend Development | Auth APIs, database integration |
| 7 | Frontend Development | React UI, API connection |
| 8 | AI Integration | Gemini API integration |
| 9 | Feature Completion | All features complete |
| 10 | Testing | Testing report, bug fixes |
| 11 | Deployment | Live deployment |
| 12 | Documentation | Final report, user manual |
| 13 | Presentation Prep | Slides, demo |
| 14 | Final Viva | Final presentation |

---

## 📄 License

This project is developed for academic purposes as part of CSE 4104 — Software Development III at Northern University of Business and Technology, Khulna.

---

*CSE4104-7B-T06 | Northern University of Business and Technology, Khulna | 2026*


## Setup

### Backend
```bash
cd backend
npm install
cp .env.example .env
npm run dev
```

### Frontend
```bash
cd frontend
npm install
cp .env.example .env
npm run dev
```

# 🤖 AI Interview Preparation Platform

<div align="center">

### 🚀 AI-Powered Personalized Interview Preparation Platform

An intelligent full-stack web application that uses **Google Gemini AI** to analyze a candidate's resume, self-description, and target job description and generate a personalized interview preparation experience.

Built with the **MERN Stack**, modern authentication, document processing, AI-powered analysis, and personalized career preparation workflows.

</div>

---

## 📌 Overview

The **AI Interview Preparation Platform** is a full-stack application designed to help candidates prepare for technical and behavioral interviews in a personalized way.

Traditional interview preparation often requires candidates to manually identify relevant skills, search for interview questions, analyze job descriptions, and create preparation plans.

This platform brings these processes together into a single intelligent workflow.

The candidate provides:

- 📄 Resume
- 👤 Self Description
- 💼 Target Job Description

The system processes this information and uses **Google Gemini AI** to generate a personalized interview report containing:

- Technical interview questions
- Behavioral interview questions
- Question intentions
- Suggested answers
- Skill-gap analysis
- Personalized preparation plan
- Interview matching score

The platform can also generate an **AI-assisted resume PDF** based on the candidate's information and target role.

---

# ✨ Key Features

## 🔐 Authentication & User Management

The platform provides secure user authentication and account management.

### Features

- User registration
- User login
- JWT-based authentication
- Secure password hashing
- Authentication middleware
- Protected API routes
- Cookie-based authentication
- User-specific interview reports
- Logout functionality

---

## 🛠️ Technology Stack

| Category | Technologies | Purpose |
|---|---|---|
| **Frontend** | React, Vite, JavaScript, HTML5, CSS3 | Building the interactive user interface |
| **Backend** | Node.js, Express.js | Building the server-side application and REST APIs |
| **Database** | MongoDB, Mongoose | Storing users, interview reports, skill gaps, and preparation plans |
| **AI / GenAI** | Google Gemini API, Google GenAI SDK | AI-powered interview analysis, question generation, skill-gap analysis, and personalized preparation |
| **Authentication** | JWT, bcrypt, Cookie Parser | Secure user authentication, password hashing, and session/token management |
| **API Communication** | Axios, REST APIs | Communication between the React frontend and Express backend |
| **File Upload** | Multer | Handling resume PDF uploads |
| **Document Processing** | PDF Parser | Extracting text from uploaded resume PDFs |
| **PDF Generation** | HTML-based PDF generation | Generating downloadable AI-assisted resume PDFs |
| **Validation** | Zod | Validating structured AI responses and application data |
| **Cross-Origin Security** | CORS | Secure communication between frontend and backend |
| **Development Tools** | npm, Git, GitHub | Dependency management, version control, and source-code hosting |
| **Environment Management** | `.env` / Environment Variables | Securely managing API keys, database URLs, and authentication secrets |
| **Architecture** | MERN Stack, REST Architecture, Service-Based Backend | Structuring the application into scalable frontend, backend, database, and AI layers |



## 📑 AI-Generated Resume PDF

The platform also provides functionality for generating an AI-assisted resume PDF.

The system uses:
Candidate Information
        +
Resume
        +
Target Job Description
        ↓
Google Gemini AI
        ↓
Structured Resume HTML
        ↓
PDF Generation
        ↓
Downloadable Resume PDF
This allows the candidate to create a resume targeted toward a particular job opportunity.

----
# 📄 Resume Processing

Candidates can upload their resume in PDF format.


### Resume Workflow

```text
Candidate
    ↓
Upload Resume PDF
    ↓
Backend receives file
    ↓
PDF text extraction
    ↓
Resume content processing
    ↓
AI analysis
    ↓
Personalized Interview Report
```

## 🏗️ System Architecture
The application follows a modern full-stack architecture.

                         ┌───────────────────────┐
                         │       User            │
                         │                       │
                         │ Resume                │
                         │ Self Description      │
                         │ Job Description       │
                         └───────────┬───────────┘
                                     │
                                     ▼
                         ┌───────────────────────┐
                         │      React Frontend   │
                         │                       │
                         │ UI / Forms / Pages    │
                         │ API Communication      │
                         └───────────┬───────────┘
                                     │
                                     │ HTTP Requests
                                     ▼
                         ┌───────────────────────┐
                         │    Express Backend    │
                         │                       │
                         │ Routes                │
                         │ Controllers           │
                         │ Middleware            │
                         │ Services              │
                         └───────┬───────┬───────┘
                                 │       │
                    ┌────────────┘       └─────────────┐
                    ▼                                  ▼
          ┌──────────────────┐                ┌──────────────────┐
          │    MongoDB       │                │ Google Gemini AI │
          │                  │                │                  │
          │ Users            │                │ AI Analysis      │
          │ Interview Reports│                │ Questions        │
          └──────────────────┘                │ Skill Gaps       │
                                              │ Preparation Plan │
                                              └──────────────────┘
----

## 📁 Project Structure
```text
interview-ai/
│
├── Backend/
│   │
│   ├── src/
│   │   │
│   │   ├── config/
│   │   │   └── database.js
│   │   │
│   │   ├── controllers/
│   │   │   ├── auth.controller.js
│   │   │   └── interview.controller.js
│   │   │
│   │   ├── middlewares/
│   │   │   └── auth.middleware.js
│   │   │
│   │   ├── models/
│   │   │   ├── user.model.js
│   │   │   ├── interviewReport.model.js
│   │   │   └── blacklist.model.js
│   │   │
│   │   ├── routes/
│   │   │   ├── auth.routes.js
│   │   │   └── interview.routes.js
│   │   │
│   │   ├── services/
│   │   │   └── ai.service.js
│   │   │
│   │   └── app.js
│   │
│   ├── .gitignore
│   ├── package.json
│   ├── package-lock.json
│   └── server.js
│
│
├── Frontend/
│   │
│   ├── public/
│   │
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── services/
│   │   ├── assets/
│   │   └── ...
│   │
│   ├── .gitignore
│   ├── package.json
│   ├── package-lock.json
│   ├── vite.config.js
│   └── index.html
│
│
├── .gitignore
├── package-lock.json
└── README.md
```
---



## 👩‍💻 Author
Avani Gupta

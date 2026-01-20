Job Portal Application
📋 Overview
A full-stack job portal application built with the MERN stack (MongoDB, Express.js, React.js, Node.js) featuring role-based authentication for job seekers and recruiters, with Cloudinary integration for file uploads.

✨ Features
🤝 For Job Seekers
Browse and search job listings

Apply for jobs with resume upload

Track application status

Save favorite jobs

Profile management with skills and experience

🏢 For Recruiters
Post and manage job listings

Review applicant profiles

Manage application status

Company profile management

Dashboard with analytics

🛠️ Tech Stack
Backend
Node.js & Express.js - Server framework

MongoDB - Database with Mongoose ODM

JWT - Authentication & authorization

bcryptjs - Password encryption

Cloudinary - Image/video file uploads

Multer - File handling middleware

Frontend
React.js - UI library

React Router - Navigation

Context API - State management

Axios - HTTP client

CSS Modules - Styling

📁 Project Structure
Backend (/backend)
text
backend/
├── controllers/     # Business logic for routes
├── models/         # MongoDB schemas
├── routes/         # API endpoints
├── middlewares/    # Auth & error handling
├── database/       # DB connection config
├── utils/          # Helper functions
├── app.js          # Express app configuration
└── server.js       # Server entry point
Frontend (/frontend)
text
frontend/src/
├── components/     # Reusable components
│   ├── Auth/      # Login/Register components
│   ├── Home/      # Landing page components
│   ├── Job/       # Job-related components
│   └── Layout/    # Layout components
├── pages/         # Page components
└── main.jsx       # App entry point
🚀 Quick Start
Prerequisites
Node.js (v14 or higher)

MongoDB (Local or Atlas)

Cloudinary account

npm or yarn package manager

1. Clone Repository
bash
git clone <repository-url>
cd job-portal
2. Backend Setup
bash
cd backend
npm install
Create .env file:

env
PORT=5000
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key
JWT_EXPIRE=7d
CLOUDINARY_CLOUD_NAME=your_cloudinary_name
CLOUDINARY_API_KEY=your_cloudinary_api_key
CLOUDINARY_API_SECRET=your_cloudinary_api_secret
NODE_ENV=development
3. Frontend Setup
bash
cd frontend
npm install
Create .env file:

env
VITE_API_URL=http://localhost:5000/api
4. Run Application
Start backend:

bash
cd backend
npm start
Start frontend:

bash
cd frontend
npm run dev
Access the application at http://localhost:5173

🌐 API Endpoints
Authentication
POST /api/auth/register - User registration

POST /api/auth/login - User login

GET /api/auth/me - Get current user

Jobs
GET /api/jobs - Get all jobs (with filters)

GET /api/jobs/:id - Get single job

POST /api/jobs - Create job (Recruiter only)

PUT /api/jobs/:id - Update job (Recruiter only)

DELETE /api/jobs/:id - Delete job (Recruiter only)

Applications
POST /api/applications - Apply for job

GET /api/applications/my-applications - Get user's applications

GET /api/applications/job/:id - Get job applications

PUT /api/applications/:id - Update application status

☁️ Cloudinary Integration
The application uses Cloudinary for:

User profile pictures

Company logos

Resume/CV uploads

Job-related media files

Files are uploaded directly from the client to Cloudinary using secure signed uploads.

🔐 Security Features
JWT-based authentication

Password hashing with bcrypt

Protected API routes

Role-based access control (Job Seeker/Recruiter)

Input validation and sanitization

File type and size validation

📱 Key Pages
Landing Page (/)
Hero section with call-to-action

Job search functionality

Popular categories and companies

Dashboard (/dashboard)
Job seeker: Applied jobs, saved jobs, recommendations

Recruiter: Posted jobs, applicant statistics

Job Listings (/jobs)
Filter and search jobs

Job cards with key details

Pagination support

Job Details (/jobs/:id)
Complete job description

Company information

Apply/Save functionality

🗄️ Database Models
User
Name, email, password (hashed)

Role (jobseeker/recruiter)

Profile information

Skills, experience (for job seekers)

Company details (for recruiters)

Job
Title, description, requirements

Company, location, salary

Job type, experience level

Posted by (recruiter reference)

Application
Job reference

Applicant reference

Resume/CV file URL

Cover letter

Application status

🚧 Development
Code Style
ESLint for code linting

Prettier for code formatting

Consistent naming conventions

Version Control
Git for version control

Feature branch workflow

Conventional commits

🤝 Contributing
Fork the repository

Create a feature branch (git checkout -b feature/AmazingFeature)

Commit your changes (git commit -m 'Add some AmazingFeature')

Push to the branch (git push origin feature/AmazingFeature)

Open a Pull Request
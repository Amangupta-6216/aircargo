Air Cargo Booking & Tracking System
A full-stack web application designed for managing air cargo bookings, flight route search, and real-time shipment tracking. This project demonstrates modern frontend, backend, and database design with strong security, modular architecture, and clean development practices.

🚀 Project Overview
The Air Cargo Booking and Tracking System enables users to:

Register and authenticate securely

Search available flight routes

Create cargo bookings

Track shipment status in real-time

Manage user dashboard and booking history

🧱 System Architecture
Three-Tier Architecture
Frontend: React + TypeScript + Material-UI

Backend: Node.js + Express

Database: PostgreSQL

Authentication: JWT

ORM: Sequelize / TypeORM

scss
Copy code
Frontend (React)
        ↕
Backend (Node.js/Express)
        ↕
Database (PostgreSQL)
📁 Project Structure
css
Copy code
air-cargo/
├── backend/
│   ├── src/
│   │   ├── controllers/
│   │   ├── models/
│   │   ├── services/
│   │   ├── middleware/
│   │   └── routes/
│   └── package.json
└── frontend/
    ├── src/
    │   ├── components/
    │   ├── pages/
    │   ├── store/
    │   └── services/
    └── package.json
⚙️ Features
1. User Authentication
Register/Login using email & password

Password hashing (bcrypt)

JWT-based session management

Protected backend routes

2. Flight Route Search
Direct + one-stop flight detection

Validates time constraints

Displays airline, timings, and connections

3. Cargo Booking
Create booking with weight, pieces, origin, destination

Multi-flight route selection

Automatic reference ID generation

Booking history retrieval

4. Real-Time Tracking
Timeline of events:
Created → Departed → Arrived → Delivered

Updates stored in timeline_events table

5. Secure & Efficient Backend
Validation using Joi

Sanitized SQL queries

Global error handler

PostgreSQL indexes for performance

🗄️ Database Design
Main Tables
Table	Description
users	Registered user data
airlines	Airline info
flights	Flight details
bookings	Cargo bookings
timeline_events	Tracking updates

🌐 API Endpoints
Method	Endpoint	Description
POST	/api/v1/auth/signup	Register user
POST	/api/v1/auth/login	Login user
GET	/api/v1/routes	Search flights
POST	/api/v1/bookings	Create booking
GET	/api/v1/bookings/my-bookings	Get user bookings
GET	/api/v1/bookings/:id/history	Shipment history

🧩 Key Algorithms
Flight Route Search Logic
Finds direct flights

Generates one-stop connecting routes

Ensures valid time ordering

Booking Reference Generator
Generates unique IDs like:

scss
Copy code
AC + timestamp(base36) + random(base36)
🛡️ Security Implementation
bcrypt password hashing

JWT token authentication

SQL injection prevention using parameterized queries

Validation using JOI schemas

Centralized error handler

🖥️ Frontend (React + TypeScript)
Architecture
Component-based

Redux store for global state

API service layer using fetch

Lazy loading and memoization for performance

Main Components
Login / Signup

Dashboard

Booking Page

Tracking Page

🧪 Testing
Backend Tests
Jest + Supertest

Unit tests for controllers

Integration tests for API endpoints

Manual UI Testing
Browser compatibility tests

Form validation

Workflow testing (booking → tracking)

🛠️ Setup Instructions
Backend Setup
arduino
Copy code
cd backend
npm install
npm run dev
Frontend Setup
powershell
Copy code
cd frontend
npm install
npm start
🗃️ Database Setup Options
Option 1 — Cloud PostgreSQL (No Installation Required)
Recommended free-tier services:

Supabase

ElephantSQL

NeonDB

Railway

Set in .env:

bash
Copy code
DATABASE_URL=postgresql://user:pass@host/db
Option 2 — Using Docker
Copy code
docker-compose up -d
Option 3 — Hybrid (SQLite for dev / PostgreSQL for prod)
ini
Copy code
DB_TYPE=sqlite
SQLITE_PATH=./database.sqlite
🚀 Deployment
Environment Variables
ini
Copy code
NODE_ENV=production
PORT=3000
JWT_SECRET=yourSecretKey
DATABASE_URL=postgresql://...
CORS_ORIGIN=https://yourdomain.com
Build
arduino
Copy code
npm run build
npm run migrate:prod
📈 Future Enhancements
Email notifications

Mobile app development

Real airline API integration

Payment gateway for paid cargo services

Microservices architecture

Caching using Redis

🏁 Conclusion
This project demonstrates:

✔ Full-stack development
✔ Modern React patterns
✔ Secure Node.js API design
✔ Clean database schema with PostgreSQL
✔ Real-time event tracking
✔ Professional-level system design

The Air Cargo Booking & Tracking System is fully functional and ready for demonstration as an academic or portfolio project.


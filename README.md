# GEPSys: AI-Powered Philippine Government Procurement Search

GEPSys is a full-stack web application designed to simplify the process of searching for Philippine government procurement opportunities. It leverages an AI-powered assistant to understand natural language queries and provides a real-time, user-friendly interface for exploring over 23,000 procurement notices.

## Key Features

*   **AI-Powered Search:** Uses OpenAI's GPT-4 with Function Calling to parse natural language queries and translate them into precise database searches.
*   **Real-time Data:** A Node.js scraper keeps the PostgreSQL database updated with the latest data from PhilGEPS.
*   **Modern Frontend:** A responsive and interactive user interface built with React and Tailwind CSS.
*   **Secure Authentication:** OTP-based email login system using JWT for secure, stateless sessions.
*   **Admin Dashboard:** A comprehensive dashboard for monitoring system metrics, managing users, and controlling the data scraper.

---

## Technical Architecture & Environment

### **Core Technology Stack**

*   **Frontend:** React 18, JavaScript ES6+, Tailwind CSS, React Router
*   **Backend:** Node.js 18+, Express.js, PostgreSQL 14+, JWT, Nodemailer, WebSockets
*   **Database:** PostgreSQL with full-text search (`ts_vector`) and JSONB support.
*   **AI & Integration:** OpenAI GPT-4, Web Scraping, `node-cron` for scheduling.

### **Project Structure**

```
GEPSys/
├── frontend/       # React SPA (UI)
├── backend/        # Node.js/Express Server (API)
├── .gitignore      # Files to be ignored by Git
└── README.md       # This file
```

### **Environment Variables**

The backend requires a `.env` file for local development with the following keys:

```env
# Server & Database
NODE_ENV=development
PORT=5000
DB_HOST=localhost
DB_DATABASE=gepsys_db
DB_USER=postgres
DB_PASSWORD=your_password
DB_PORT=5432

# Authentication & Email
JWT_SECRET=your_jwt_secret
EMAIL_USER=your_email@gmail.com
EMAIL_PASS=your_app_password

# AI Integration
OPENAI_API_KEY=your_openai_key
```

---

## Development Setup

1.  **Clone the repository.**
2.  **Setup Backend:**
    ```bash
    cd backend
    npm install
    # Create and populate .env file
    npm start
    ```
3.  **Setup Frontend:**
    ```bash
    cd frontend
    npm install
    npm start
    ```
The application will be running locally with the frontend on `http://localhost:3000` and the backend on `http://localhost:5000`.

---

## Project History & Milestones

*   **January 11, 2025 - System Stabilization:**
    *   Successfully implemented and fixed the OTP email authentication system using Nodemailer and Gmail.
    *   Resolved all backend infrastructure issues, including API endpoint routing and database schema alignment.
    *   Stabilized the Admin Dashboard, fixing data display and state management bugs.
    *   System is now fully operational with secure authentication and a working admin panel.

*   **July 6, 2025 - Admin Dashboard Finalization:**
    *   Completed all admin modules: Key Metrics, Scraper Control, Log Viewer, and User Management.
    *   Wrote and passed a comprehensive suite of tests for all dashboard components.

*   **July 2, 2025 - AI Assistant Production Deployment:**
    *   Successfully deployed the production-grade AI Assistant with advanced multi-filter query support.
    *   Optimized natural language processing for Philippine-specific locations and contexts.
    *   Confirmed real-time data access to over 23,000 opportunities.

*(For a more detailed history, please refer to the Git commit log.)*
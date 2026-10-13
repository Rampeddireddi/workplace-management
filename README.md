# Workplace Efficiency & Sustainability Dashboard

A role-aware workforce analytics dashboard for employee, manager, and HR access levels. The application combines an Express.js backend with a React + Vite frontend and uses Recharts for all charts and KPI visualizations.

## Features

- Role-based dashboard and protected routes
- Five KPI sections: meeting effectiveness, office utilization, engagement, learning participation, and hybrid work effectiveness
- People directory restricted to authorized roles
- Individual employee KPI summaries and scoped access checks
- Sustainability analytics as a secondary analytics section
- In-memory demo data and mock authentication for rapid local testing

## Prerequisites

- Node.js 18+
- npm

## Local setup

1. Install backend dependencies:
   ```bash
   cd backend
   npm install
   ```

2. Install frontend dependencies:
   ```bash
   cd ../frontend
   npm install
   ```

3. Start the backend API:
   ```bash
   cd ../backend
   npm start
   ```

4. Start the frontend app:
   ```bash
   cd ../frontend
   npm run dev
   ```

5. Open the app in your browser at http://localhost:5173

## Demo accounts

These demo accounts are available for testing access rules:

- HR: EMP001 / demo-hr-2024
- Manager: EMP005 / demo-manager-2024
- Employee: EMP006 / demo-emp1-2024

## API overview

- POST /api/auth/login
- POST /api/auth/logout
- GET /api/auth/me
- GET /api/auth/demo-accounts
- GET /api/dashboard
- GET /api/reports/:kpi
- GET /api/people
- GET /api/people/:employeeId
- GET /api/health

## Scripts

Backend:

```bash
cd backend
npm start
npm test
```

Frontend:

```bash
cd frontend
npm run dev
npm run build
npm run test
```

## Notes

- The dashboard uses in-memory JavaScript data and mock sessions for demo purposes.
- Authorization is enforced both in the frontend route guards and the backend middleware.
- Recharts is the only charting library used in the project.

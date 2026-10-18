# Recipe Book API

Express.js + TypeScript backend for the Recipe Book app, using PostgreSQL (Neon) with Drizzle ORM.

**Live API:** https://recipe-book-backend-j1v9.onrender.com
**Frontend:** https://recipe-book-frontend-pi.vercel.app

## Features
- Signup, login, refresh-token rotation and logout (JWT in HttpOnly cookies)
- CSRF protection on auth and cookie-based requests
- Role-based access: USER (recipe CRUD on own recipes) and ADMIN (view all recipes)
- Request validation with Zod

## Tech Stack
Express 5, TypeScript, Drizzle ORM, Neon PostgreSQL, JWT, csrf-csrf, Zod

## Setup
1. Install dependencies:
```bash
   npm install
```
2. Create a `.env` file in the project root:
```
   APP_NAME=Recipe Book API
   PORT=7000
   NODE_ENV=development
   JWT_SECRET=<your secret>
   CSRF_SECRET=<your secret>
   BACKEND_URL=http://localhost:7000
   FRONTEND_URL=http://localhost:5173
   DATABASE_URL=<your Neon connection string>
```
3. Apply the database schema:
```bash
   npm run db:plan
   npm run db:migrate
```
4. Start the dev server:
```bash
   npm run dev
```

## Scripts
| Command | Purpose |
|---|---|
| `npm run dev` | Start in development mode |
| `npm run build` | Build to `dist/` |
| `npm start` | Run the production build |
| `npm run db:plan` | Generate a migration from the schema |
| `npm run db:migrate` | Apply migrations |
| `npm run db:studio` | Open Drizzle Studio |

## Deployment (Render)
- Build: `npm install --include=dev && npm run build`
- Start: `npm start`
- Set `NODE_ENV=production`, `FRONTEND_URL` (exact Vercel URL), `BACKEND_URL`, `DATABASE_URL`, `JWT_SECRET`, `CSRF_SECRET`.

## Team
- <Member 1>
- <Member 2>
- <Member 3>
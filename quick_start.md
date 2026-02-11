# AJCE Website - Quick Start Guide

## 🚀 Current Project Status

### ✅ What's Already Built
Projects scaffold with complete architecture:

```
✓ Backend Express Server (TypeScript)
✓ Next.js 14 Frontend 
✓ Static Data (No MongoDB Required!) ⭐ NEW
✓ In-Memory Contact Form Storage
✓ API Routes & Controllers
✓ Tailwind CSS Design System
✓ 8 Core Pages (Home, Courses, Depts, Faculty, Events, Contact, About, Admissions)
✓ Reusable React Components (Navbar, Footer, Cards)
✓ Custom Hooks (useData, useForm)
✓ API Client & Auth Store (Zustand)
✓ Docker Removed - Simplified Setup!
```

**⭐ MAJOR UPDATE:** This project now runs **WITHOUT MongoDB or Docker**! See [STATIC_DATA_MODE.md](STATIC_DATA_MODE.md) for details.

### 📦 Project Structure
```
Website_AJCE/
├── server/                          # Backend
│   ├── src/
│   │   ├── config/database.ts       # MongoDB connection
│   │   ├── models/                  # Mongoose schemas  
│   │   ├── controllers/             # Business logic
│   │   ├── routes/                  # API endpoints
│   │   ├── middleware/              # Auth, errors
│   │   ├── utils/                   # Helper functions
│   │   └── index.ts                 # Express server
│   ├── seeds/seedData.ts            # Sample data
│   ├── package.json
│   └── tsconfig.json
│
├── client/                          # Frontend  
│   ├── src/
│   │   ├── app/                     # Next.js pages
│   │   ├── components/              # React components
│   │   ├── hooks/                   # Custom hooks
│   │   ├── lib/                     # API client, stores
│   │   └── styles/                  # Global CSS
│   ├── tailwind.config.ts
│   ├── next.config.js
│   └── package.json
│
├── README.md                        # Project overview
└── DEVELOPMENT_PLAN.md              # This comprehensive plan
```

---

## ⚡ Getting Started Locally

### Prerequisites
- **Node.js 18+** → https://nodejs.org/
- **Git** → https://git-scm.com/

**That's it!** No MongoDB, Docker, or additional setup needed!

### Optional (for adding to documentation only)
- **Docker** (if you want to containerize later)
- **MongoDB** (if you want to add persistence features later)

### Step 1: Run Setup Script

**Windows:**
```bash
cd c:\Website_AJCE
setup.bat
```

**Mac/Linux:**
```bash
cd ~/Website_AJCE
chmod +x setup.sh
./setup.sh
```

This automatically:
- ✅ Checks Node.js installation
- ✅ Installs backend dependencies
- ✅ Installs frontend dependencies
- ✅ Creates `.env` files from templates

### Step 2: Configure Database

**Option A: MongoDB Atlas (Recommended - Free Cloud)**
1. Go to https://www.mongodb.com/cloud/atlas
2. Create free account
3. Create M0 cluster (free tier)
4. Get connection string
5. Add to `server/.env`:
```
MONGO_URI=mongodb+srv://username:password@cluster.mongodb.net/ajce?retryWrites=true&w=majority
```

### Step 2: Update Environment Files (Optional)

The project works with default settings, but you can customize:

**Server (.env)**
```bash
PORT=5000
NODE_ENV=development
FRONTEND_URL=http://localhost:3000
CORS_ORIGIN=http://localhost:3000
```

**Frontend (.env.local)**
```bash
NEXT_PUBLIC_API_URL=http://localhost:5000/api
```

### Step 3: No Database Setup Needed!

✅ Static data is already included in `server/src/data/staticData.ts`  
✅ Contact form stores in memory (per session)  
✅ No MongoDB or Docker required!

For details on static data, see [STATIC_DATA_MODE.md](STATIC_DATA_MODE.md)

### Step 4: Run Servers

**Backend** (Terminal 1)
```bash
cd server
npm start
```

You'll see:
```
✅ Server running on http://localhost:5000
🗂️  Static Data Mode - No MongoDB required
```

**Frontend** (Terminal 2)
```bash
cd client
npm run dev
```

You'll see:
```
> Ready in 1.2s
> Local: http://localhost:3000
```

### Step 5: Access Your Website

- **Frontend:** http://localhost:3000
- **API:** http://localhost:5000/api
- **Health Check:** http://localhost:5000/api/health

---

## 📊 Static Data Available

All data pre-loaded without database:

**Departments** (3)
- Computer Science & Engineering
- Electronics & Communication Engineering  
- Mechanical Engineering

**Courses** (4)
- Data Structures & Algorithms
- Database Management Systems
- Digital Communications
- Thermodynamics

**Faculty** (4)
- Dr. Rajesh Kumar (CSE)
- Prof. Anil Sharma (CSE)
- Dr. Priya Menon (EC)
- Prof. Suresh Nair (ME)

**Events** (3)
- Tech Conference 2024
- Summer Workshop
- Annual Hackathon

See [STATIC_DATA_MODE.md](STATIC_DATA_MODE.md) for API details and filtering options.

---

## 🎯 Quick Development Checklist

### Setup Phase
- [ ] Download Node.js 18+ from https://nodejs.org/
- [ ] Extract project or clone from GitHub
- [ ] Run `npm install` in server and client folders
- [ ] Start backend: `cd server && npm start`
- [ ] Start frontend: `cd client && npm run dev`
- [ ] Access http://localhost:3000

**Effort:** 15-20 minutes

### Testing Phase
- [ ] View departments at http://localhost:3000/departments
- [ ] View courses at http://localhost:3000/courses
- [ ] View faculty at http://localhost:3000/faculty
- [ ] Test contact form at http://localhost:3000/contact
- [ ] Check API endpoints at http://localhost:5000/api

**Effort:** 10 minutes

### Next Steps
1. Customize data in `server/src/data/staticData.ts`
2. Add MongoDB if you need data persistence (see [STATIC_DATA_MODE.md](STATIC_DATA_MODE.md))
3. Deploy to Vercel (frontend) & Railway/Render (backend)
4. See [DEVELOPMENT_PLAN.md](DEVELOPMENT_PLAN.md) for full roadmap

**Total Setup Time:** ~30 minutes

---

## 📝 Important Files to Review

### Backend Files

| File | Purpose |
|------|---------|
| [server/src/index.ts](server/src/index.ts) | Express app setup, routes registration |
| [server/src/data/staticData.ts](server/src/data/staticData.ts) | All static data (departments, courses, faculty, events) |
| [server/src/controllers/](server/src/controllers/) | Business logic (uses staticData) |
| [server/src/routes/](server/src/routes/) | API endpoints |

### Frontend Files

| File | Purpose |
|------|---------|
| [client/src/app/page.tsx](client/src/app/page.tsx) | Home page |
| [client/src/app/courses/page.tsx](client/src/app/courses/page.tsx) | Courses listing |
| [client/src/app/departments/page.tsx](client/src/app/departments/page.tsx) | Departments |
| [client/src/components/layout/](client/src/components/layout/) | Layout components |
| [client/src/lib/api.ts](client/src/lib/api.ts) | API client setup |
| [client/tailwind.config.ts](client/tailwind.config.ts) | Design system |

---

## 🔧 Common Commands

### Backend
```bash
cd server

npm install               # Install dependencies
npm start                # Start server (default: port 5000)
npm run dev              # Start with auto-reload
npm run build            # Build TypeScript
npm run lint             # Check code quality
```

### Frontend
```bash
cd client

npm install              # Install dependencies
npm run dev              # Start dev server (default: port 3000)
npm run build            # Build for production
npm run start            # Run production build
npm run lint             # ESLint check
npm run type-check       # TypeScript check
```

---

## 🚨 Troubleshooting

### Issue: Port Already in Use
**Solution:**
```bash
# Windows: Find and kill process on port 3000
netstat -ano | findstr :3000
taskkill /PID <PID> /F

# Or change port in .env:
PORT=5001
NEXT_PUBLIC_API_URL=http://localhost:5001/api
```

### Issue: API 404 Errors on Frontend
**Solution:**
- Verify backend is running: `curl http://localhost:5000/api/health`
- Check NEXT_PUBLIC_API_URL in client/.env.local
- Clear browser cache (Ctrl + Shift + Delete)
- Backend server must be running before frontend

### Issue: Module Not Found Errors
**Solution:**
```bash
# Clear node_modules and reinstall
rimraf node_modules package-lock.json
npm install
```

### Issue: Contact Form Data Lost
**Solution (Expected Behavior):**
- ✅ This is normal! Contact data is stored in memory
- Data is lost when server restarts
- To persist: Add MongoDB or file storage (see [STATIC_DATA_MODE.md](STATIC_DATA_MODE.md))

### Issue: CORS Errors
**Solution:**
- Ensure both frontend and backend are running
- Check FRONTEND_URL in server/.env matches client URL
- Check CORS_ORIGIN in .env is correct

---

## 📚 Key Technologies & Docs

### Backend
- **Express.js**: https://expressjs.com/ (Web framework)
- **TypeScript**: https://www.typescriptlang.org/ (Type safety)
- **Static Data**: server/src/data/staticData.ts (No database needed)

### Frontend
- **Next.js 14**: https://nextjs.org/ (React framework)
- **React 18**: https://react.dev/ (UI library)
- **Tailwind CSS**: https://tailwindcss.com/ (Styling)
- **React Query**: https://tanstack.com/query/latest (Data fetching)

---

## 🎨 Design System Colors

Use these in components:
```css
Primary:   #0284c7 (Sky Blue)
Secondary: #f59e0b (Amber)
Dark:      #075985 (Navy)
Success:   #10b981 (Green)
Error:     #ef4444 (Red)
Warning:   #f59e0b (Amber)
```

---

## ✨ Next Steps After Getting Started

1. **Customize Static Data**
   - Edit `server/src/data/staticData.ts` with your college data
   - Update departments, courses, faculty, events

2. **Customize Frontend**
   - Update colors in `client/tailwind.config.ts`
   - Modify components in `client/src/components/`
   - Update pages in `client/src/app/`

3. **Add Database (Optional)**
   - Follow [STATIC_DATA_MODE.md](STATIC_DATA_MODE.md) Section "Moving to Production"
   - Set up MongoDB Atlas if you need persistence
   - Deploy to production platforms (Vercel, Railway, Render, etc.)

4. **For Full Development Plan**
   - See [DEVELOPMENT_PLAN.md](DEVELOPMENT_PLAN.md) for 14-week roadmap
   - Phase 1: Foundation (DONE ✅)
   - Phase 2: Feature development
   - Phase 3: Advanced features
   - Phase 4-5: Testing & Launch

---

## 📞 Support & Questions

- Check [DEVELOPMENT_PLAN.md](DEVELOPMENT_PLAN.md) Section 11 for API endpoints
- Review README.md for architecture overview
- Check component files for usage examples
- Review existing pages for patterns

---

**Status:** Ready for Development  
**Last Updated:** February 10, 2026  
**Estimated Launch:** 14 weeks from start

# 📘 AJCE College Website

> **🎉 MAJOR UPDATE:** This project now runs **WITHOUT MongoDB or Docker!** Just Node.js 18+ is needed.

A modern, sleek, youth-centric responsive website for **Amal Jyothi College of Engineering (AJCE)** — fully rebuilt using **Next.js 14**, **React 18**, **Express.js**, and **TypeScript**. This project enhances the official college site ([https://www.ajce.in/](https://www.ajce.in/)) with dynamic features and elegant UI/UX inspired by Harvard & Cambridge.

**⚡ Status:** Static Data Mode Ready ✅  
**🚀 Quick Start:** 30 minutes to running locally  
**📅 Timeline:** 14-week development plan  
**📚 Documentation:** See [QUICK_START.md](QUICK_START.md) for setup  
**💻 Requirements:** Node.js 18+ only - No MongoDB, No Docker needed!

---

## ⭐ What's Special

### Static Data Mode (NEW!)
✅ **No MongoDB Required** - All data hardcoded in `server/src/data/staticData.ts`  
✅ **No Docker Required** - Simple Node.js + npm setup  
✅ **In-Memory Contact Form** - Contact submissions stored during session  
✅ **Ready for Production** - Easy to add database later if needed  
✅ **Perfect for Demos** - Works instantly on any machine with Node.js  

### What's Built
✅ Complete backend API (Express + TypeScript)  
✅ Next.js 14 frontend with modern design system  
✅ Static/hardcoded data (departments, courses, faculty, events)  
✅ 8 core pages (Home, Courses, Departments, Faculty, Events, Contact, About, Admissions)  
✅ Reusable component library (Navbar, Footer, Cards)  
✅ Tailwind CSS design system with modern colors  
✅ API filtering & query parameters  
✅ Contact form with in-memory storage

---

## 🚀 Quick Start (30 minutes)

### 1. Prerequisites
- **Download Node.js 18+:** https://nodejs.org/
- **That's it!** No MongoDB, Docker, or other tools needed

### 2. Setup
```bash
cd c:\Website_AJCE
setup.bat              # Windows
# OR
chmod +x setup.sh && ./setup.sh  # Mac/Linux
```

### 3. Run
**Terminal 1 - Backend:**
```bash
cd server
npm start
# Server running on http://localhost:5000
```

**Terminal 2 - Frontend:**
```bash
cd client
npm run dev
# Open http://localhost:3000
```

### 4. Done! 🎉
- Frontend: http://localhost:3000
- API: http://localhost:5000/api
- Health: http://localhost:5000/api/health

For detailed setup, see [QUICK_START.md](QUICK_START.md) and [STATIC_DATA_MODE.md](STATIC_DATA_MODE.md)

---

## 📚 Documentation

| Document | Purpose |
|----------|---------|
| [QUICK_START.md](QUICK_START.md) | **START HERE** - Setup & first run |
| [STATIC_DATA_MODE.md](STATIC_DATA_MODE.md) | API endpoints, data structure, limitations |
| [ENV_SETUP_GUIDE.md](ENV_SETUP_GUIDE.md) | Environment variables reference |
| [DEVELOPMENT_PLAN.md](DEVELOPMENT_PLAN.md) | 14-week roadmap & feature list |
| [API_TESTING_GUIDE.md](API_TESTING_GUIDE.md) | How to test API endpoints |
| [DEPLOYMENT_GUIDE.md](DEPLOYMENT_GUIDE.md) | Deploy to production |

---

## 📦 Project Structure & Features

### Architecture

```
Frontend (Next.js 14)          Backend (Express + TS)        Data (Static JSON)
- Pages: 8 core pages          - RESTful API                 - departments.json
- Components: 20+ reusable     - Controllers & Services      - courses.json
- Hooks: Data fetching         - Middleware: Logging         - faculty.json
- State: Zustand + React Query - Routes: API endpoints       - events.json
```

### Technology Stack

**Backend:**
- Express.js 4.18+ (REST API)
- TypeScript 5.1+ (Type safety)
- Node.js 18+ (Runtime)
- CORS enabled

**Frontend:**
- Next.js 14 (React framework)
- React 18 (UI library)
- Tailwind CSS 3.3+ (Styling)
- React Query (Data fetching)
- Zustand (State management)

**No External Dependencies:**
- ✅ No MongoDB
- ✅ No Docker
- ✅ No authentication/JWT needed for demo
- ✅ No email service
- ✅ No third-party APIs

### 🎨 Implemented Pages & Features

#### 1. **🏠 Home**
- Hero section with CTA buttons
- Feature cards (4 highlights)
- Statistics counter
- Call-to-action section
- Smooth animations (Framer Motion)

#### 2. **📚 Courses**
- Course listing with grid layout
- Filters: **Level (UG/PG), Department, Semester**
- Course cards with metadata
- Details: credits, semester, department badge
- Responsive design (mobile → desktop)

#### 3. **🏛️ Departments**
- Department cards with HOD info
- Faculty count per department
- Location & contact info
- Phone & email links
- Department detail pages (coming)

#### 4. **👨‍🎓 Faculty Directory**
- Faculty member cards with photos
- **Filter by: Department, Role**
- Contact info (email, phone)
- Bio & role
- Faculty profile pages (coming)

#### 5. **📅 Events**
- Upcoming events listing
- **Filter by: Category, Active Status**
- Event details (date, location, capacity)
- Category badges
- Registration CTAs
- Event detail pages (coming)

#### 6. **📋 Contact**
- Contact form with validation ✅
- Department selection
- **In-memory storage** (stored during session)
- Contact info cards (phone, email, location)
- Social media links

#### 7. **ℹ️ About**
- Mission & vision statements
- Accreditations & recognition
- Key features (6 highlights)
- College heritage

#### 8. **📝 Admissions**
- Program offerings (B.Tech, M.Tech)
- Admission process (6 steps)
- Important dates section
- FAQs (4 common questions)
- Apply CTA

---

## 📊 Static Data Available

All pre-loaded without any database:

### Departments (3)
- Computer Science & Engineering (CSE)
- Electronics & Communication Engineering (EC)
- Mechanical Engineering (ME)

Each with:
- HOD information
- Faculty members list
- Contact info
- Location & labs

### Courses (4)
- Data Structures & Algorithms (UG, Sem 3)
- Database Management Systems (UG, Sem 3)
- Digital Communications (PG, Sem 3)
- Thermodynamics (UG, Sem 4)

Each with:
- Level, Semester, Credits
- Department affiliation
- Course code
- Description

### Faculty (4)
- Dr. Rajesh Kumar (CSE)
- Prof. Anil Sharma (CSE)
- Dr. Priya Menon (EC)
- Prof. Suresh Nair (ME)

Each with:
- Department & Role
- Contact info
- Qualifications

### Events (3)
- Tech Conference 2024
- Summer Workshop
- Annual Hackathon

### News/Articles (3)
- Latest happenings
- Student achievements
- Industry partnerships

See [STATIC_DATA_MODE.md](STATIC_DATA_MODE.md) for complete API documentation.

### 🔧 Technical Implementation

#### Backend Components
```
✓ Express.js 4.18 + TypeScript
✓ MongoDB with Mongoose
✓ JWT Authentication
✓ Error handling middleware
✓ Seeding script with sample data
✓ 5 API route modules (departments, courses, faculty, events, contact)
✓ Controllers for business logic
✓ Utility functions (auth, validation)
```

#### Frontend Components
```
✓ Next.js 14 (App Router)
✓ React 18 with TypeScript
✓ Tailwind CSS v3.4
✓ Framer Motion animations
✓ React Query for data fetching
✓ Zustand for auth state
✓ Radix UI + Lucide Icons
✓ Responsive layout components
```

#### Design System
```
Colors:
  Primary:   #0284c7 (Sky Blue)
  Secondary: #f59e0b (Amber) 
  Dark:      #075985 (Navy)
  Neutral:   Gray scale

Typography:
  Headlines: Inter Bold (5xl, 4xl, 3xl)
  Body:      Inter Regular (base, lg, sm)
  Mono:      Monaco (code)

Components:
  ✓ Buttons (Primary, Secondary, Outline)
  ✓ Cards (Course, Department, Faculty)
  ✓ Forms (Input, Select, Textarea)
  ✓ Navigation (Navbar, Footer)
  ✓ Loading states & skeletons
  ✓ Error boundaries
```

#### 🧠 **Departments**

Each department will have:

* Department overview
* **HOD profile**
* Faculty card list (name, designation, photo, short bio)
* Contact details

Example departments:

* Computer Science & Engineering
* Electronics & Communication Engineering
* Mechanical Engineering
* Civil Engineering
* Electrical & Electronics Engineering
* **(Add all departments from current AJCE menu)**

#### 👨‍🏫 **Faculty & Staff**

* List view of all teachers
* Search & filter by department
* Individual profile pages with social links

#### 🏆 Other Pages

* About Us
* Admissions
* Fee Structure
* Facilities (Library, Labs, Sports)
* Contact Us (with animated form & Google Map)
* Gallery

---

## � Getting Started

### Prerequisites
- Node.js 18+ & npm 9+
- MongoDB Atlas account (free tier works great)
- Git

### Quick Setup (5 minutes)

```bash
# 1. Clone repository
cd c:\Website_AJCE

# 2. Backend setup
cd server
npm install
cp .env.example .env
# Edit .env with MongoDB credentials

# 3. Seed database with sample data
npm run seed

# 4. Start backend (Terminal 1)
npm run dev
# Backend running: http://localhost:5000

# 5. Frontend setup (Terminal 2)
cd client
npm install
cp .env.local.example .env.local

# 6. Start frontend
npm run dev
# Frontend running: http://localhost:3000
```

### Verify Installation
- Home page: http://localhost:3000
- Courses: http://localhost:3000/courses
- API health check: http://localhost:5000/api/health

**Complete setup guide:** See [QUICK_START.md](QUICK_START.md)

---

## 📋 Tech Stack Details

### Backend
```
├── Framework: Express.js 4.18
├── Language: TypeScript 5.3
├── Database: MongoDB with Mongoose
├── Authentication: JWT (7-day expiry)
├── Validation: express-validator
├── Security: bcryptjs, CORS, rate limiting
└── Environment: dotenv, ts-node-dev
```

### Frontend  
```
├── Framework: Next.js 14 (App Router)
├── Library: React 18 with TypeScript
├── Styling: Tailwind CSS 3.4
├── State: Zustand + React Query
├── Animations: Framer Motion 10.16
├── Icons: Lucide React 0.292
├── Components: Radix UI
└── Utilities: clsx, axios
```

### DevOps Ready
```
├── Version Control: Git + GitHub
├── CI/CD: GitHub Actions workflow
├── Frontend: Vercel deployment
├── Backend: Render/Railway deployment  
├── Database: MongoDB Atlas (cloud)
├── CDN: Cloudflare integration
└── Monitoring: Sentry + custom logging
```

---

## 📊 Project Timeline

| Phase | Duration | Focus | Status |
|-------|----------|-------|--------|
| **Phase 1: Foundation** | Weeks 1-3 | Core pages, setup | ✅ Complete |
| **Phase 2: Features** | Weeks 4-6 | Detail pages, admin | 🚀 Starting |
| **Phase 3: Engagement** | Weeks 7-9 | Search, blog, email | 📅 Upcoming |
| **Phase 4: Polish** | Weeks 10-12 | Testing, optimization | 📅 Upcoming |
| **Phase 5: Launch** | Weeks 13-14 | Deploy, monitor | 📅 Upcoming |

**Complete roadmap:** See [DEVELOPMENT_PLAN.md](DEVELOPMENT_PLAN.md)

---

## 📁 Project Structure

```
Website_AJCE/
├── server/                              # Node.js + Express backend
│   ├── src/
│   │   ├── config/
│   │   │   └── database.ts              # MongoDB connection
│   │   ├── models/                      # Mongoose schemas
│   │   │   ├── User.ts
│   │   │   ├── Department.ts
│   │   │   ├── Course.ts
│   │   │   ├── Event.ts
│   │   │   ├── News.ts
│   │   │   └── Contact.ts
│   │   ├── controllers/                 # Business logic
│   │   │   ├── departmentController.ts
│   │   │   ├── courseController.ts
│   │   │   ├── facultyController.ts
│   │   │   ├── eventController.ts
│   │   │   └── contactController.ts
│   │   ├── routes/                      # API endpoints
│   │   │   ├── departments.ts
│   │   │   ├── courses.ts
│   │   │   ├── faculty.ts
│   │   │   ├── events.ts
│   │   │   └── contact.ts
│   │   ├── middleware/
│   │   │   ├── auth.ts                  # JWT authentication
│   │   │   └── errorHandler.ts
│   │   ├── utils/
│   │   │   └── auth.ts                  # JWT, bcrypt utilities
│   │   └── index.ts                     # Express app entry point
│   ├── seeds/
│   │   └── seedData.ts                  # Sample data generator
│   ├── package.json
│   ├── tsconfig.json
│   ├── .env.example
│   └── README.md
│
├── client/                              # Next.js 14 frontend
│   ├── src/
│   │   ├── app/                         # Page routes
│   │   │   ├── layout.tsx               # Root layout
│   │   │   ├── page.tsx                 # Home page
│   │   │   ├── courses/
│   │   │   │   └── page.tsx
│   │   │   ├── departments/
│   │   │   │   └── page.tsx
│   │   │   ├── faculty/
│   │   │   │   └── page.tsx
│   │   │   ├── events/
│   │   │   │   └── page.tsx
│   │   │   ├── contact/
│   │   │   │   └── page.tsx
│   │   │   ├── about/
│   │   │   │   └── page.tsx
│   │   │   └── admissions/
│   │   │       └── page.tsx
│   │   ├── components/
│   │   │   ├── layout/
│   │   │   │   ├── Navbar.tsx
│   │   │   │   └── Footer.tsx
│   │   │   ├── cards/
│   │   │   │   ├── CourseCard.tsx
│   │   │   │   ├── DepartmentCard.tsx
│   │   │   │   └── FacultyCard.tsx
│   │   │   └── forms/                   # Form components (Phase 2)
│   │   ├── hooks/
│   │   │   ├── useData.ts               # Data fetching hooks
│   │   │   └── useForm.ts               # Form handling hook
│   │   ├── lib/
│   │   │   ├── api.ts                   # API type definitions
│   │   │   ├── apiClient.ts             # Axios configuration
│   │   │   └── authStore.ts             # Zustand auth store
│   │   └── styles/
│   │       └── globals.css              # Tailwind + custom styles
│   ├── public/                          # Static assets
│   ├── tailwind.config.ts
│   ├── next.config.js
│   ├── tsconfig.json
│   ├── package.json
│   ├── .env.local.example
│   └── README.md
│
├── README.md                            # This file
├── QUICK_START.md                       # Setup instructions
├── DEVELOPMENT_PLAN.md                  # 20-section comprehensive plan
└── .gitignore
```

---

## 🔌 API Endpoints

### Public Routes
```
GET  /api/health                    Health check
GET  /api/departments               List departments
GET  /api/departments/:id           Department details
GET  /api/courses                   List courses (filterable)
GET  /api/courses/:id               Course details  
GET  /api/faculty                   List faculty (filterable)
GET  /api/faculty/:id               Faculty profile
GET  /api/events                    List events
GET  /api/events/:id                Event details
POST /api/contact                   Submit contact form
```

### Protected Routes (Admin)
```
POST   /api/departments             Create department
PUT    /api/departments/:id         Update department
DELETE /api/departments/:id         Delete department

POST   /api/courses                 Create course
PUT    /api/courses/:id             Update course
DELETE /api/courses/:id             Delete course

POST   /api/faculty                 Create faculty
PUT    /api/faculty/:id             Update faculty
DELETE /api/faculty/:id             Delete faculty

GET    /api/admin/contacts          View all contacts
PATCH  /api/admin/contacts/:id      Mark as read
DELETE /api/admin/contacts/:id      Delete contact
```

**Full API documentation:** See [DEVELOPMENT_PLAN.md](DEVELOPMENT_PLAN.md) Section 5

---

## 🎨 Design Inspiration

This website draws design inspiration from:
- **Harvard University:** https://www.harvard.edu
- **Cambridge University:** https://www.cam.ac.uk
- **MIT:** https://www.mit.edu
- **Stanford:** https://www.stanford.edu

Key design principles implemented:
✅ Minimalist, elegant aesthetic  
✅ Strong typography hierarchy  
✅ Ample whitespace & breathing room  
✅ Smooth animations & transitions  
✅ Mobile-first responsive design  
✅ Clear call-to-action buttons  
✅ Intuitive navigation structure  
✅ Accessibility-first approach
---

## 🎓 Sample Data Included

The `/seeds/seedData.ts` script populates your database with:

```
✓ 3 Departments (CSE, EC, ME)
✓ 10+ Faculty members with roles
✓ 3+ Sample courses (UG & PG)
✓ 2 Sample events
✓ Admin account: admin@ajce.in / Admin@12345
✓ Sample faculty: rajesh.kumar@ajce.in / Faculty@123
```

Generated sample photos use placeholder service for rapid prototyping.

---

## 💻 Common Development Commands

### Backend
```bash
cd server

npm run dev              # Start dev server with hot reload
npm run build           # Compile TypeScript
npm start               # Run compiled server
npm run seed            # Populate sample data
npm run lint            # Check code quality
```

### Frontend
```bash
cd client

npm run dev             # Development server
npm run build           # Production build
npm run start           # Serve production build  
npm run lint            # ESLint check
npm run type-check      # Type checking
```

---

## 🔐 Security Features

✅ **Authentication**
- JWT tokens with 7-day expiry
- bcryptjs password hashing
- Refresh token rotation (planned)

✅ **Authorization**
- Role-based access control (RBAC)
- Admin-only operations protected
- Faculty-level permissions

✅ **API Security**
- CORS properly configured
- Rate limiting (100 req/min)
- Input validation & sanitization
- XSS protection (CSP headers)

--- 

## 📈 Performance Targets

| Metric | Target |
|--------|--------|
| Largest Contentful Paint (LCP) | < 2.5s |
| First Input Delay (FID) | < 100ms |
| Cumulative Layout Shift (CLS) | < 0.1 |
| Page Load Time | < 2.5s |
| API Response (p95) | < 200ms |
| Uptime SLA | 99.9% |

---

## 🐛 Environment Variables

### Server (.env)
```
MONGO_URI=mongodb+srv://user:pass@cluster.mongodb.net/ajce
PORT=5000
JWT_SECRET=your_super_secret_jwt_key
NODE_ENV=development
FRONTEND_URL=http://localhost:3000
```

### Client (.env.local)
```
NEXT_PUBLIC_API_URL=http://localhost:5000/api
```

---

## 📚 Documentation

- **[DEVELOPMENT_PLAN.md](DEVELOPMENT_PLAN.md)** — 20-section comprehensive roadmap
- **[QUICK_START.md](QUICK_START.md)** — Fast setup & troubleshooting
- **[API Documentation](DEVELOPMENT_PLAN.md#5-api-endpoints)** — Endpoint reference
- **Code Comments** — Inline documentation

---

## 🤝 Contributing

We welcome contributions! Please:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit changes (`git commit -m 'Add amazing feature'`)
4. Push branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

See [DEVELOPMENT_PLAN.md](DEVELOPMENT_PLAN.md) for architectural guidelines.

---

## 📞 Support & Questions

- Check documentation files first
- Review existing component implementations
- Check API endpoint definitions
- See [QUICK_START.md](QUICK_START.md) troubleshooting section

---

## � Complete Documentation Guide

We've prepared comprehensive guides for every phase of development. Start with the one that matches your needs:

### 🚀 Getting Started
- **[QUICK_START.md](./QUICK_START.md)** ← Start here! (5-minute setup)
  - Local development setup
  - Essential commands
  - Troubleshooting tips
  
- **[INDEX.md](./INDEX.md)** - Documentation roadmap
  - Complete guide to all docs
  - Workflow quick links
  - Technology stack overview

### 📋 Development
- **[DEVELOPMENT_PLAN.md](./DEVELOPMENT_PLAN.md)** - Full 14-week roadmap
  - Project vision & 5-phase timeline
  - Database schema (30+ fields)
  - Complete API specification (30+ endpoints)
  - Security & performance targets
  - Team structure & budget

- **[CONTRIBUTING.md](./CONTRIBUTING.md)** - How to contribute
  - Code style guide (TypeScript, React best practices)
  - Commit message format
  - PR process
  - Testing requirements

### 🐳 Setup & Local Development
- **[DOCKER_GUIDE.md](./DOCKER_GUIDE.md)** - Docker & containerization
  - Quick start with `docker-compose up`
  - All service configurations
  - Development workflow
  - Troubleshooting containers

- **[ENV_SETUP_GUIDE.md](./ENV_SETUP_GUIDE.md)** - Environment configuration
  - All environment variables (backend & frontend)
  - MongoDB Atlas setup
  - Secret generation
  - Security best practices

### 🌐 Deployment & DevOps
- **[DEPLOYMENT_GUIDE.md](./DEPLOYMENT_GUIDE.md)** - Production deployment
  - Vercel frontend setup
  - Render backend setup
  - MongoDB Atlas configuration
  - DNS & SSL setup
  - CI/CD pipeline explanation
  - Monitoring & disaster recovery

- **[GITHUB_SECRETS_SETUP.md](./GITHUB_SECRETS_SETUP.md)** - CI/CD configuration
  - GitHub Actions secrets setup
  - Render & Vercel token configuration
  - Step-by-step secret creation

### 🧪 Testing & API
- **[API_TESTING_GUIDE.md](./API_TESTING_GUIDE.md)** - Complete API reference
  - All 30+ endpoints documented
  - Request/response examples
  - cURL commands for testing
  - Postman import instructions
  - Sample credentials for testing

### ⚙️ Automation
- **[setup.sh](./setup.sh)** - Auto setup (Linux/Mac)
  ```bash
  chmod +x setup.sh && ./setup.sh
  ```

- **[setup.bat](./setup.bat)** - Auto setup (Windows)
  ```cmd
  setup.bat
  ```

### 📦 Infrastructure
- **[Dockerfile](./server/Dockerfile)** - Backend containerization
- **[Dockerfile](./client/Dockerfile)** - Frontend containerization
- **[docker-compose.yml](./docker-compose.yml)** - Local multi-container setup
- **[.github/workflows/ci-cd.yml](./.github/workflows/ci-cd.yml)** - GitHub Actions pipeline

---

## 🎯 Quick Navigation by Use Case

**❓ "I want to set up locally"**
→ [QUICK_START.md](./QUICK_START.md) (5 min) or [DOCKER_GUIDE.md](./DOCKER_GUIDE.md)

**🚀 "I want to deploy"**
→ [DEPLOYMENT_GUIDE.md](./DEPLOYMENT_GUIDE.md) → [GITHUB_SECRETS_SETUP.md](./GITHUB_SECRETS_SETUP.md)

**📖 "I want to understand the architecture"**
→ [DEVELOPMENT_PLAN.md](./DEVELOPMENT_PLAN.md) (see Sections 1-5)

**💻 "I want to contribute code"**
→ [CONTRIBUTING.md](./CONTRIBUTING.md) (code standards & workflow)

**🔌 "I want to test the API"**
→ [API_TESTING_GUIDE.md](./API_TESTING_GUIDE.md) (all endpoints with examples)

**⚙️ "I want to configure environment"**
→ [ENV_SETUP_GUIDE.md](./ENV_SETUP_GUIDE.md) + [GITHUB_SECRETS_SETUP.md](./GITHUB_SECRETS_SETUP.md)

**🐳 "I want to use Docker"**
→ [DOCKER_GUIDE.md](./DOCKER_GUIDE.md) + `docker-compose up`

---

## ℹ️ Phase Status & Timeline

| Phase | Name | Status | Duration | Features |
|-------|------|--------|----------|----------|
| 1 | Foundation | ✅ Complete | Weeks 1-3 | Backend API, frontend pages, auth, design system |
| 2 | Feature Development | 🚀 In Progress | Weeks 4-6 | Detail pages, admin dashboard, search |
| 3 | Polish & Optimization | ⏳ Planned | Weeks 7-8 | Performance, SEO, accessibility |
| 4 | Testing & QA | ⏳ Planned | Weeks 9-11 | Unit tests, E2E tests, security audit |
| 5 | Deployment & Launch | ⏳ Planned | Weeks 12-14 | Staging, production, monitoring |

**Phase 1 Deliverables:** 18 backend files + 15 frontend files + 10 documentation guides = Foundation Complete ✅

---

## �📄 License

MIT License © 2026 Amal Jyothi College of Engineering

---

## 🙏 Acknowledgments

- Design inspiration: Harvard, Cambridge, MIT, Stanford universities
- Open source community: Next.js, Express, MongoDB, Tailwind teams
- Icons: Lucide React
- Animations: Framer Motion

---

## 📞 Official Reference

AJCE Official Website: [https://www.ajce.in/](https://www.ajce.in/)

---

**Status:** Phase 1 Complete ✅ | Phase 2 Starting 🚀  
**Last Updated:** February 10, 2026  
**Estimated Launch:** 14 weeks from start (May 2026)


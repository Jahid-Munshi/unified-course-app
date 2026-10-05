# 🎓 Unified Course App (UCA)

> **A Unified Course Discovery & Comparison Platform for Learners in Bangladesh and Global Curriculums.**

[![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=flat&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Next.js](https://img.shields.io/badge/Next.js%2015-black?style=flat&logo=next.js&logoColor=white)](https://nextjs.org/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=flat&logo=tailwind-css&logoColor=white)](https://tailwindcss.com/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=flat&logo=postgresql&logoColor=white)](https://www.postgresql.org/)
[![License: Private](https://img.shields.io/badge/License-Proprietary-red.svg)](LICENSE)

---

## 📌 Executive Summary & Business Problem

Learners in Bangladesh (students, job seekers, and working professionals) face huge fragmentation when researching educational programs. Whether searching for a **GRE preparation course**, an **IT bootcamp**, or **professional certifications**, learners spend countless hours scouring hundreds of distinct national and international platforms without a standardized way to compare them.

**The Unified Course App solves this by providing:**
- A single consolidated directory of thousands of verified courses.
- Side-by-side comparison across pricing, duration, curriculum, and delivery format.
- Intelligent cross-lingual search enabling Bengali keyword queries to match English course titles.
- Authentic aspect-based user ratings highlighting both **positive and negative aspects (pros and cons)** of each course.

---

## 🚀 Key In-Scope Features (FR-01 — FR-12)

- 🔍 **Cross-Lingual Search (FR-07, FR-08, FR-09):** Search courses using Bengali terms and phonetics with automatic semantic mapping to English course titles.
- 🎛️ **Multi-Criteria Dynamic Filtering (FR-01, FR-02, FR-03):** Simultaneous filtering by category/subject, pricing, user rating, duration, location, and learning format.
- ⚖️ **Side-by-Side Comparison Engine (FR-10):** Direct side-by-side comparison matrix for up to 4 courses.
- ⭐ **Aspect-Based Reviews & Ratings (FR-11, FR-12):** Verified student reviews with breakdown of positive vs. negative aspects.
- 🏢 **Course Provider Profiles & Outbound Links:** Profiles of national and international providers with direct referral links.
- 📱 **Mobile-Responsive UI (NFR):** Optimized for seamless performance on desktop, tablet, and mobile devices.

---

## 🛠️ Technology Stack

| Layer | Technology | Purpose |
| :--- | :--- | :--- |
| **Frontend Framework** | Next.js 15 (App Router, React 19) | Server-Side Rendering (SSR) for SEO, dynamic client interactivity |
| **Language** | TypeScript | End-to-end type safety between frontend, APIs, and database |
| **Styling** | Tailwind CSS + shadcn/ui | Modern, responsive, utility-first UI design |
| **Database** | PostgreSQL | Relational modeling, indexing, ACID transactions |
| **ORM** | Prisma / Drizzle | Type-safe database queries & migrations |
| **Search Engine** | PostgreSQL Full-Text Search (`pg_trgm`) | Bilingual text matching & typo-tolerant fuzzy search |
| **Authentication** | NextAuth.js / Auth.js | Secure user sessions, learner profiles, and role management |

---

## 👥 Core Project Team

| Team Member | Role | Primary Focus Area |
| :--- | :--- | :--- |
| **Jahid** | Full-Stack / Lead Developer | Architecture, API routes, database modeling, and comparison engine |
| **Aishwarya** | Frontend Developer | Responsive UI/UX, filter drawer, cross-lingual search UI, and client state |
| **Saima** | Backend & QA Developer | Course data ingestion pipelines, aspect review engine, testing, and security |

---

## 📅 Project Timeline

- **Project Kickoff:** October 5, 2026
- **Target Production Launch:** January 20, 2027
- **Planned Work Effort:** 1,280.0 Hours across 5 execution phases

---

## 📂 Repository Structure

```
unified-course-app/
├── .github/
│   ├── ISSUE_TEMPLATE/
│   │   ├── bug_report.md
│   │   └── feature_request.md
│   └── pull_request_template.md
├── src/
│   ├── app/                 # Next.js App Router (pages and API routes)
│   │   ├── api/             # REST / Server Actions
│   │   ├── courses/         # Course catalog & detail views
│   │   ├── compare/         # Side-by-side comparison page
│   │   └── providers/       # Provider directory & profiles
│   ├── components/          # Reusable UI components (search, cards, filters)
│   ├── lib/                 # Utility functions, database client, search helpers
│   ├── types/               # Shared TypeScript interfaces & models
│   └── styles/              # Global styles and Tailwind configuration
├── prisma/                  # Database schema and migration scripts
├── public/                  # Static assets (icons, logos, placeholders)
├── .env.example             # Template for environment variables
├── .gitignore
├── CONTRIBUTING.md          # Team branching & PR guidelines
└── README.md
```

---

## 💻 Getting Started Locally

### Prerequisites
- Node.js 20.x or higher
- PostgreSQL 15.x or higher
- Git

### Installation
1. Clone the private repository:
   ```bash
   git clone https://github.com/<your-username>/unified-course-app.git
   cd unified-course-app
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Configure environment variables:
   ```bash
   cp .env.example .env.local
   # Update DATABASE_URL and NEXTAUTH_SECRET in .env.local
   ```

4. Run database migrations:
   ```bash
   npx prisma migrate dev
   ```

5. Start the development server:
   ```bash
   npm run dev
   ```

6. Open [http://localhost:3000](http://localhost:3000) in your browser.

---

## 🌿 Git Branching Strategy

- `main` — Production-ready code. Direct pushes are protected.
- `develop` — Integration branch for sprint deliverables.
- `feature/<feature-name>` — Individual feature branches (e.g., `feature/bengali-search-parser`).
- `bugfix/<issue-name>` — Bug resolution branches.

All changes must go through a **Pull Request (PR)** and require at least 1 peer approval before merging.

# SkillMatch AI – Industry Skill & Curriculum Alignment Platform

**Problem Statement ID:** 26134  
**Title:** Challenges in aligning skill development programs with industry requirements and emerging job market demands.

---

## 🎯 Project Goal

**SkillMatch AI** addresses the structural disconnect between engineering/higher-education curricula and current industry hiring demands. The platform empowers students and academic institutions to:
1. **Track Industry Demand:** Monitor verified skill requirements, salary brackets, and demand intensities across modern tech roles.
2. **Detect Competency Gaps:** Run automated, interactive skill-gap analyses comparing current student profiles with target industry job requirements.
3. **Recommend Certified Bridge Courses:** Provide personalized course pathways (NPTEL, Coursera, Meta, AWS, Stanford Online) to close missing skill gaps.
4. **Manage Academic Profiles:** Track student portfolios, verified skills, and diagnostic histories.

---

## 🛠️ Tech Stack & Architecture

- **Frontend & Routing:** Next.js 14 (App Router)
- **Language:** TypeScript
- **Styling & Theme:** Tailwind CSS (Dark Mode & Professional Slate/Indigo Design System)
- **Visualizations:** Recharts (Interactive comparative analytics)
- **Icons:** Lucide React
- **Database Layer:** MongoDB with Mongoose (Ready with schemas & client connection helper)

---

## 📁 Folder Structure

```
c:\mini project.1\
├── .vscode\
│   └── launch.json                # VS Code debug launcher configured for http://localhost:3000
├── src\
│   ├── app\
│   │   ├── layout.tsx             # Root layout with responsive Sidebar and Header
│   │   ├── globals.css            # Dark theme styling, glow utilities, and custom scrollbar
│   │   ├── page.tsx               # 1. Executive Alignment Dashboard
│   │   ├── industry-demand\
│   │   │   └── page.tsx           # 2. Industry Demand Page (Search, Filter, Job Cards)
│   │   ├── skill-gap-analyzer\
│   │   │   └── page.tsx           # 3. Interactive Skill Gap Analyzer
│   │   ├── courses\
│   │   │   └── page.tsx           # 4. Course Recommendations & Catalog
│   │   └── profile\
│   │       └── page.tsx           # 5. Student Competency & Academic Profile
│   ├── components\
│   │   ├── Sidebar.tsx            # Persistent sidebar with 5 core navigation routes
│   │   ├── Header.tsx             # Header breadcrumbs, status tags, and cycle indicator
│   │   └── DashboardCharts.tsx    # Recharts dual-bar chart & trending skills meters
│   ├── data\
│   │   └── mockData.ts            # Realistic industry job roles, trending skills & courses
│   ├── lib\
│   │   └── mongodb.ts             # Cached MongoDB connection helper with graceful fallback
│   ├── models\
│   │   ├── JobRole.ts             # Mongoose schema for Job Roles
│   │   ├── Course.ts              # Mongoose schema for Courses
│   │   └── SkillGap.ts            # Mongoose schema for Saved Skill Gap diagnostics
│   └── types\
│       └── index.ts               # Complete TypeScript interface definitions
├── package.json
├── tsconfig.json
├── tailwind.config.ts
└── README.md
```

---

## 🚀 Implemented Modules

### 1. 📊 Executive Alignment Dashboard (`/`)
- **KPI Metrics:** Total Job Roles, High-Demand Skills, Average Curriculum Gap (42%), Recommended Courses.
- **Industry Demand vs. Curriculum Readiness Chart:** Dual-bar comparative graph across 6 major tech domains.
- **Top 5 Trending Skills:** Real-time popularity ranking, demand index scores (up to 98/100), and YoY growth percentages.
- **Quick-launch Navigation Banners:** Direct deep-links to analysis and course modules.

### 2. 📈 Industry Demand Page (`/industry-demand`)
- **Role Profiles:** Job roles with title, category, description, required skills badges, salary brackets, openings count, and growth rates.
- **Demand Levels:** Visual badges for High / Medium / Low demand tiers.
- **Location & Experience:** Remote/Hybrid/On-site and Entry/Mid/Senior experience filters.
- **Live Search & Filter Toolbar:** Real-time instant filtering.
- **Direct Gap Check:** One-click launch into the Gap Analyzer for any specific job role.

### 3. 🎯 Skill Gap Analyzer (`/skill-gap-analyzer`)
- **Target Role Selection:** Select target job profile from dropdown or URL query parameters.
- **Current Skills Manager:** Clickable skills cloud, custom tag input, and one-click student presets (*CS 3rd Year Student*, *Self-Taught Web Dev*, *Data Science Enthusiast*).
- **Interactive Analyze Button:** Computes alignment metrics with smooth state feedback.
- **Detailed Diagnostic Output:**
  - **Match Score %** & **Skill Gap %**
  - Dual-gradient visual competency meter
  - **Matched Skills List** (Green checkmark badges)
  - **Missing Skills List** (Amber/Rose alert badges)
  - Direct **Course Bridge CTA** filtering courses specifically for missing skills.

### 4. 🎓 Course Recommendations (`/courses`)
- **Bridge Courses:** Certified courses from NPTEL, Stanford Online, Meta, AWS, DeepLearning.AI, and Google.
- **Course Details:** Title, Provider, Skill Covered badge, Duration, Difficulty level, Rating, and key syllabus highlights.
- **Priority Indicator:** *Highly Recommended*, *Curriculum Core*, and *Career Booster* tags.
- **Interactive Filter Bar:** Filter by missing skill tags, difficulty level, priority, or search term.
- **Bookmark Action:** Save courses directly to your academic profile.

### 5. 👤 Student Competency & Academic Profile (`/profile`)
- **Academic Credentials:** Degree, college/university, current semester, CGPA status, and verified student tag.
- **Active Skills Inventory:** Editable list of student competencies with proficiency levels and verification tags.
- **Target Career Goals:** Primary and secondary career tracks.
- **Diagnostic History:** Log of past skill-gap analyses.
- **Enrolled & Bookmarked Courses:** Quick access to saved bridge courses.

---

## 💻 How to Run Locally

### Prerequisites
- [Node.js](https://nodejs.org/) (v18.x or higher)
- npm (v9.x or higher)

### Step 1: Open Terminal in Project Directory
```bash
cd "c:\mini project.1"
```

### Step 2: Install Dependencies (if not already installed)
```bash
npm install
```

### Step 3: Start Development Server
```bash
npm run dev
```

### Step 4: Open in Web Browser
Visit [http://localhost:3000](http://localhost:3000) to interact with the working platform.

*(Optional)* If you want to connect to a live MongoDB instance, create a `.env.local` file with:
```env
MONGODB_URI=mongodb+srv://<username>:<password>@cluster.mongodb.net/skillmatch
```
If `MONGODB_URI` is omitted, the application automatically uses the built-in realistic mock dataset.

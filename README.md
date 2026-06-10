# 🏗️ Project Analysis Framework
### A Solo Full-Stack Developer's Pre-Development Playbook

> **কোড লেখার আগে এই document সম্পূর্ণ করুন।**
> Figma Designer যেভাবে ডিজাইন শুরু করার আগে সব analyze করে, আপনিও সেভাবে।

---

## 📋 Table of Contents

1. [Business Analysis](#1-business-analysis)
2. [Competitor Research](#2-competitor-research)
3. [User Personas](#3-user-personas)
4. [User Flow Design](#4-user-flow-design)
5. [Sitemap](#5-sitemap)
6. [Feature Breakdown](#6-feature-breakdown)
7. [Page Inventory](#7-page-inventory)
8. [Section Structure](#8-section-structure)
9. [Content Hierarchy](#9-content-hierarchy)
10. [Wireframe Planning](#10-wireframe-planning)
11. [Design System](#11-design-system)
12. [Database Schema](#12-database-schema)
13. [API Planning](#13-api-planning)
14. [Development Roadmap](#14-development-roadmap)
15. [MVP Definition](#15-mvp-definition)
16. [Pre-Development Checklist](#-pre-development-checklist)
17. [AI Mega-Prompt](#-ai-mega-prompt)

---

## 1. Business Analysis

**উদ্দেশ্য:** Client কী বানাতে চায় এবং কেন — সেটা একদম পরিষ্কার করা।

### Client থেকে জানতে হবে

| প্রশ্ন | উত্তর |
|--------|-------|
| এই প্রজেক্টের উদ্দেশ্য কী? | |
| কারা ব্যবহার করবে? | |
| ব্যবহারকারীরা কী কাজ করতে পারবে? | |
| Revenue Model কী? (Subscription / One-time / Freemium) | |
| কারা Competitor? | |
| Success কীভাবে measure হবে? | |
| Budget এবং Timeline কী? | |

### এই Step-এর Output

```
Business Goal    : [এক লাইনে]
Problem Statement: [User কোন সমস্যায় আছে?]
Solution         : [এই প্রজেক্ট কীভাবে সমাধান দেবে?]
Target Audience  : [Primary + Secondary]
Revenue Model    : [কীভাবে টাকা আসবে?]
```

---

## 2. Competitor Research

**উদ্দেশ্য:** Market কী করছে সেটা দেখে নিজের product কোথায় দাঁড়াবে বোঝা।

### ন্যূনতম ৫টি Competitor বিশ্লেষণ করুন

| Competitor | URL | Strength | Weakness | Opportunity |
|------------|-----|----------|----------|-------------|
| 1. | | | | |
| 2. | | | | |
| 3. | | | | |
| 4. | | | | |
| 5. | | | | |

### প্রতিটি Competitor-এ এগুলো দেখুন

- **Navigation Structure** — কোন menu, কোন flow?
- **Hero Section** — কী CTA, কী headline?
- **Feature Presentation** — কীভাবে features দেখাচ্ছে?
- **Pricing Page** — কী model, কী tier?
- **Onboarding Flow** — Register → Dashboard পর্যন্ত কটা step?
- **Design Style** — Color, font, spacing কেমন?

### এই Step-এর Output

```
Market Gap    : [কোন জায়গায় সবাই weak?]
Differentiation: [আমাদের product কোথায় আলাদা হবে?]
Design Direction: [কোন competitor-এর design আমাদের inspire করবে?]
```

---

## 3. User Personas

**উদ্দেশ্য:** কার জন্য বানাচ্ছি সেটা concrete করা — assumptions নয়, real profiles।

### Persona Template

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
PERSONA 1: [Name]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Role       : [Student / Manager / Admin]
Age Range  : [18-25 / 30-45]
Tech Level : [Beginner / Intermediate / Advanced]

Goals
  → [লক্ষ্য ১]
  → [লক্ষ্য ২]

Pain Points
  → [সমস্যা ১]
  → [সমস্যা ২]

Devices    : [Mobile / Desktop / Both]
Use Context: [কোথায় use করবে? Work / Home / On-the-go]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

> 📌 **Tip:** Primary persona-র জন্য design করুন, secondary persona-র জন্য accommodate করুন।

---

## 4. User Flow Design

**উদ্দেশ্য:** User কোন path-এ navigate করবে সেটা map করা।

### Main Flow (Happy Path)

```
[Entry Point]
     ↓
[Landing Page]
     ↓
[Sign Up / Login]
     ↓
[Onboarding / Dashboard]
     ↓
[Core Action] ← এটাই প্রজেক্টের মূল কাজ
     ↓
[Success / Confirmation]
```

### Alternative Flows

```
Unauthenticated User → Protected Page → Redirect to Login → Return to original page
Forgot Password → Email OTP → Reset → Login
Free User → Premium Feature → Upgrade Prompt → Checkout
```

### Edge Cases

```
□ Empty State (data নেই)
□ Error State (API fail)
□ Loading State
□ Permission Denied
□ Session Expired
```

---

## 5. Sitemap

**উদ্দেশ্য:** পুরো প্রজেক্টের page structure একনজরে দেখা।

```
📁 PUBLIC
├── /                    (Home)
├── /about
├── /features
├── /pricing
├── /blog
│   └── /blog/:slug
└── /contact

📁 AUTH
├── /login
├── /register
└── /forgot-password

📁 USER DASHBOARD
├── /dashboard
├── /profile
├── /settings
│   ├── /settings/account
│   └── /settings/billing
└── /[core-feature-pages]

📁 ADMIN PANEL
├── /admin
├── /admin/users
├── /admin/content
└── /admin/reports
```

> 📌 প্রতিটি route-এর জন্য: কে access করতে পারবে (Public / Auth / Admin) সেটা mark করুন।

---

## 6. Feature Breakdown

**উদ্দেশ্য:** কী কী functionality থাকবে সেটা role-অনুযায়ী আলাদা করা।

### Public Features

- [ ] Landing page দেখা
- [ ] Blog/Content পড়া
- [ ] Contact form পাঠানো
- [ ] Pricing দেখা

### User (Authenticated) Features

- [ ] Register / Login / Logout
- [ ] Profile manage করা
- [ ] [Core Feature 1]
- [ ] [Core Feature 2]
- [ ] Notifications দেখা
- [ ] Subscription/Billing manage করা

### Admin Features

- [ ] User list, search, ban/unban
- [ ] Content create/edit/delete
- [ ] Analytics dashboard দেখা
- [ ] Settings configure করা

---

## 7. Page Inventory

**উদ্দেশ্য:** কতটি page বানাতে হবে এবং প্রতিটির কী কী component দরকার।

| Page | Route | Access | Priority |
|------|-------|--------|----------|
| Home | `/` | Public | P1 |
| Login | `/login` | Public | P1 |
| Register | `/register` | Public | P1 |
| Dashboard | `/dashboard` | Auth | P1 |
| Profile | `/profile` | Auth | P2 |
| Admin Panel | `/admin` | Admin | P2 |
| 404 | `*` | Public | P3 |

> Priority: **P1** = MVP-তে লাগবেই | **P2** = Phase 2 | **P3** = Nice to have

---

## 8. Section Structure

**উদ্দেশ্য:** প্রতিটি page-এ কী কী section থাকবে — Figma Designer যেভাবে করে।

### 🏠 Home Page
```
1. Navbar           → Logo, Navigation Links, CTA Button
2. Hero             → Headline, Subheadline, Primary CTA, Hero Image/Video
3. Social Proof     → Trusted by X companies, Star ratings
4. Features         → 3-6টি feature card
5. How It Works     → Step-by-step process (3 steps)
6. Testimonials     → User reviews, photos
7. Pricing          → Tier comparison table
8. FAQ              → Accordion, 5-8 questions
9. Final CTA        → Bold last push
10. Footer          → Links, Legal, Social
```

### 📊 Dashboard Page
```
1. Topbar           → Search, Notifications, User Avatar
2. Sidebar          → Navigation Menu
3. Stats Overview   → KPI Cards (4টি)
4. Main Content     → [প্রজেক্টের core feature]
5. Recent Activity  → Timeline/List
```

### 🔐 Auth Pages (Login / Register)
```
1. Split Layout     → Left: Branding/Visual | Right: Form
   অথবা
   Center Card Layout → Logo, Form, Social Login, Switch link
```

> 📌 **Rule:** প্রতিটি section-এর জন্য কী **data** দরকার সেটাও লিখুন।

---

## 9. Content Hierarchy

**উদ্দেশ্য:** User page-এ এসে প্রথমে কী দেখবে, কী action নেবে।

### Hero Section Hierarchy
```
1st Eye → Headline (biggest, boldest)
2nd Eye → Subheadline (value proposition)
3rd Eye → Primary CTA Button
4th Eye → Supporting visual / Social proof
```

### Information Priority (F-Pattern Reading)
```
TOP-LEFT  → Most important (Logo, Headline)
TOP-RIGHT → Secondary action (Login, CTA)
MIDDLE    → Core content (Features, Benefits)
BOTTOM    → Trust signals, Footer
```

### CTA Strategy
```
Primary CTA   : "Get Started Free" / "Start Trial"  → Hero + Final Section
Secondary CTA : "Watch Demo" / "Learn More"          → Hero (below primary)
Inline CTA    : Feature-specific actions             → Feature cards
```

---

## 10. Wireframe Planning

**উদ্দেশ্য:** কোড করার আগে layout মাথায় clear করা।

### Tool Options
| Tool | Best For | Cost |
|------|----------|------|
| **Figma** | Full wireframe + handoff | Free/Paid |
| **Excalidraw** | Quick sketchy wireframes | Free |
| **Miro** | Collaborative flow | Free/Paid |
| **Pen & Paper** | Fastest for solo dev | Free |

### Wireframe Checklist
```
□ Mobile layout আলাদা করে ভেবেছি
□ Sidebar collapse behavior ঠিক করেছি
□ Modal/Drawer কোথায় কোথায় লাগবে
□ Empty state কেমন দেখাবে
□ Loading skeleton কোথায় থাকবে
```

> 📌 **Shortcut:** v0.dev বা Relume.io দিয়ে AI-generated wireframe নিয়ে তারপর customize করুন।

---

## 11. Design System

**উদ্দেশ্য:** Consistency — যাতে পুরো প্রজেক্টে একই look-and-feel থাকে।

### Theme Selection
```
□ Modern SaaS    (Clean, whitespace-heavy, bold typography)
□ Corporate      (Conservative, trust-focused, structured)
□ Minimal        (Less is more, high contrast)
□ Playful        (Rounded, colorful, friendly)
□ Dark Mode First
```

### Color Palette
```
Primary     : #[hex]   → CTA, Links, Active states
Secondary   : #[hex]   → Supporting elements
Accent      : #[hex]   → Highlights, badges
Background  : #[hex]   → Page background
Surface     : #[hex]   → Card/Panel background
Text Primary: #[hex]   → Headings
Text Muted  : #[hex]   → Body, captions
Success     : #22c55e
Warning     : #f59e0b
Error       : #ef4444
```

### Typography
```
Display Font : [Font Name] → Hero headlines, Big numbers
Body Font    : [Font Name] → Paragraphs, UI text
Mono Font    : [Font Name] → Code blocks, IDs

Scale:
  xs   : 12px
  sm   : 14px
  base : 16px
  lg   : 18px
  xl   : 20px
  2xl  : 24px
  3xl  : 30px
  4xl  : 36px
  5xl  : 48px
```

### Component List
```
Atoms     : Button, Input, Badge, Avatar, Icon, Spinner
Molecules : Form Field, Card, Alert, Tooltip, Dropdown
Organisms : Navbar, Sidebar, Modal, Data Table, Form
Templates : Auth Layout, Dashboard Layout, Marketing Layout
```

---

## 12. Database Schema

**উদ্দেশ্য:** Data কীভাবে store হবে সেটা আগেই ঠিক করা — পরে refactor কষ্টের।

### Entity Identification
```
প্রথমে nouns বের করুন project description থেকে:
"Users can purchase courses and track their progress"
→ Entities: User, Course, Purchase, Progress
```

### Schema Template

```
Collection/Table: users
──────────────────────────────
_id          : ObjectId
email        : String (unique, required)
passwordHash : String
role         : Enum [user, admin]
profile      : {
  name       : String
  avatar     : String (url)
  bio        : String
}
createdAt    : Date
updatedAt    : Date

──────────────────────────────

Collection/Table: [entity_name]
──────────────────────────────
_id          : ObjectId
userId       : ObjectId (ref: users)
[fields...]
status       : Enum [active, inactive, deleted]
createdAt    : Date
updatedAt    : Date
```

### Relationships
```
users        →  1:N  →  orders
orders       →  N:M  →  products
users        →  1:1  →  profile
```

---

## 13. API Planning

**উদ্দেশ্য:** Frontend এবং Backend কীভাবে communicate করবে সেটা আগে ঠিক করা।

### Convention
```
Base URL  : /api/v1
Auth      : Bearer Token (JWT) in Authorization header
Response  : { success: bool, data: {}, message: string, error?: {} }
```

### Endpoint Template

| Method | Endpoint | Auth | Description |
|--------|----------|------|-------------|
| POST | `/auth/register` | ❌ | নতুন user তৈরি |
| POST | `/auth/login` | ❌ | Login, JWT return |
| GET | `/auth/me` | ✅ | Current user info |
| GET | `/[resource]` | ✅ | List (pagination) |
| POST | `/[resource]` | ✅ | Create |
| GET | `/[resource]/:id` | ✅ | Single item |
| PUT | `/[resource]/:id` | ✅ | Update |
| DELETE | `/[resource]/:id` | ✅ Admin | Delete |

### Error Codes
```
400 → Bad Request (validation failed)
401 → Unauthorized (not logged in)
403 → Forbidden (no permission)
404 → Not Found
422 → Unprocessable Entity
500 → Server Error
```

---

## 14. Development Roadmap

**উদ্দেশ্য:** কোন কাজ কোন order-এ করব — chaos এড়ানো।

```
PHASE 1 — Foundation (Week 1)
  ✦ Project setup (Next.js / Node / DB)
  ✦ Folder structure
  ✦ Environment config (.env)
  ✦ Auth system (Register, Login, JWT, Middleware)
  ✦ Base layouts (Public, Auth, Dashboard)

PHASE 2 — Core Features (Week 2-3)
  ✦ [Core Feature 1] — CRUD + UI
  ✦ [Core Feature 2] — CRUD + UI
  ✦ Dashboard stats

PHASE 3 — Supporting Features (Week 4)
  ✦ Profile management
  ✦ Notifications
  ✦ Search & Filter
  ✦ File Upload (if needed)

PHASE 4 — Payment & Subscription (Week 5)
  ✦ Stripe / SSLCommerz integration
  ✦ Checkout flow
  ✦ Subscription management
  ✦ Webhook handling

PHASE 5 — Admin Panel (Week 6)
  ✦ User management
  ✦ Content management
  ✦ Analytics/Reports

PHASE 6 — Polish & Launch (Week 7)
  ✦ Responsive design check
  ✦ Performance optimization
  ✦ Error handling & loading states
  ✦ SEO (meta tags, OG)
  ✦ Testing
  ✦ Deployment (Vercel + Railway/Render)
```

---

## 15. MVP Definition

**উদ্দেশ্য:** কী না বানালেও চলবে — scope creep থেকে বাঁচা।

### MoSCoW Method

```
MUST HAVE (বাদ দিলে product কাজ করবে না)
  → Auth (Register/Login)
  → [Core Feature 1]
  → [Core Feature 2]
  → Basic Dashboard

SHOULD HAVE (থাকলে ভালো, না থাকলেও চলবে)
  → Notifications
  → Advanced Search
  → Profile Customization

NICE TO HAVE (Future-র জন্য রেখে দিন)
  → Dark Mode
  → Mobile App
  → Analytics Dashboard
  → Multi-language

WON'T HAVE (এই version-এ নেই)
  → AI features
  → Third-party integrations
  → [Client-র extra requests]
```

---

## ✅ Pre-Development Checklist

কোড লেখা শুরু করার আগে এই সব complete হওয়া উচিত:

```
BUSINESS
□ Business goal documented
□ Target audience defined
□ Revenue model confirmed
□ Competitor research done

PLANNING
□ User personas created (min 2)
□ User flow mapped
□ Sitemap complete
□ MVP scope locked (written, client-confirmed)

DESIGN
□ All pages listed
□ All sections per page listed
□ Content hierarchy per page noted
□ Wireframe (rough) done for main pages
□ Color palette chosen
□ Typography chosen
□ Component list ready

TECHNICAL
□ Database schema drafted
□ API endpoints listed
□ Folder structure planned
□ Tech stack confirmed
□ Deployment plan decided

BUSINESS (Client Sign-off)
□ Requirement document sent to client
□ Timeline agreed
□ Payment terms agreed
□ Scope clearly defined (to avoid scope creep)
```

---

## 🤖 AI Mega-Prompt

**যখনই নতুন প্রজেক্ট পাবেন, এই prompt copy করুন এবং `[PROJECT REQUIREMENTS]` replace করুন।**

```
Act as a Senior Product Manager, UX Designer, Solution Architect,
and Full-Stack Developer combined.

Analyze the following project requirements and generate a complete
pre-development blueprint:

1.  Business Analysis
    - Business Goal, Problem, Solution, Target Audience, Revenue Model

2.  Competitor Analysis
    - 5 competitors with Strengths, Weaknesses, Opportunities

3.  User Personas
    - 2 detailed personas with Goals, Pain Points, Devices

4.  User Flow
    - Main happy path + 3 alternative flows + edge cases

5.  Sitemap
    - Full page tree with access levels (Public/Auth/Admin)

6.  Feature List
    - Organized by role: Public / User / Admin

7.  Page Inventory
    - Each page with route, access level, priority (P1/P2/P3)

8.  Section Structure
    - Every section for every page with component details

9.  Wireframe Description
    - Text-based ASCII wireframe for Home, Dashboard, Auth pages

10. Design System
    - Theme, Color Palette (6 colors with hex), Typography, Component list

11. Database Schema
    - All collections/tables with fields, types, relationships

12. API Endpoints
    - Method, Route, Auth required, Description (table format)

13. Development Roadmap
    - Phase-by-phase breakdown with estimated time

14. MVP Scope
    - MoSCoW: Must / Should / Nice-to-have / Won't have

15. Future Scope
    - Features for v2, v3

---
Project Requirements:

[PROJECT REQUIREMENTS এখানে paste করুন]
```

---

## 💡 Quick Reference: Common Project Types

### SaaS / Dashboard Project
```
Core pages: Landing → Pricing → Auth → Dashboard → Settings
Key sections: Stats cards, Data tables, Charts, Sidebar nav
DB essentials: users, subscriptions, [core entity]
```

### E-commerce Project
```
Core pages: Home → Category → Product → Cart → Checkout → Orders
Key sections: Product grid, Filters, Product detail, Cart drawer
DB essentials: users, products, categories, orders, payments
```

### LMS / Course Platform
```
Core pages: Home → Courses → Course Detail → Lesson → Dashboard
Key sections: Course card grid, Video player, Progress tracker
DB essentials: users, courses, lessons, enrollments, progress
```

### Portfolio / Agency Site
```
Core pages: Home → About → Portfolio → Services → Contact
Key sections: Hero, Work showcase, Testimonials, CTA
DB essentials: projects, testimonials, contact_messages
```

---

*Last Updated: 2025 | Made for Freelance Full-Stack Developers*
# 🚀 The Solo Developer's Master Framework

### From Client Requirement → Figma Design → Deployment

> **একটি ফ্রেমওয়ার্ক, দুইটি ট্র্যাক।**
> প্রোজেক্টের সাইজ অনুযায়ী শুধু দরকারি ধাপগুলো ফলো করুন।

```text
                    📝 Client Requirement
                            │
            ┌───────────────┴───────────────┐
            ▼                               ▼
    🎨 DESIGN TRACK                  🛠️ DEVELOPMENT TRACK
   (ছোট প্রজেক্টের জন্য)            (বড় প্রজেক্টের জন্য)
            │                               │
            ▼                               ▼
     Figma Design Done              Database → API → Deploy
            │                               │
            └───────────────┬───────────────┘
                            ▼
                    ⚡ Development Phase
                            │
                            ▼
                    🚀 Launch Project
```

---

## 📊 Framework Usage Guide

| প্রজেক্ট টাইপ | কী কী ধাপ ফলো করবেন | সময় |
|---------------|---------------------|------|
| **Landing Page / Portfolio** | 1 → 3 → 5 → 7 → 8 → 11 | ২-৩ ঘণ্টা |
| **Small Business Website** | 1 → 2 → 3 → 5 → 7 → 8 → 11 | ৩-৪ ঘণ্টা |
| **SaaS / Dashboard** | সম্পূর্ণ ১-১৫ | ১-২ দিন |
| **E-commerce / LMS** | সম্পূর্ণ ১-১৫ | ২-৩ দিন |

---

## 🎯 Phase 1: Foundation (Design Track + Dev Track Common)

> **এই ধাপগুলো সব প্রজেক্টের জন্যই করতে হবে।**

---

### 1. Business Analysis

**উদ্দেশ্য:** Client কী বানাতে চায় এবং কেন — সেটা একদম পরিষ্কার করা।

#### Client থেকে জানতে হবে

| প্রশ্ন | উত্তর |
|--------|-------|
| প্রজেক্টের মূল উদ্দেশ্য কী? | |
| কারা ব্যবহার করবে? (Target Audience) | |
| User কী কী core task করতে পারবে? | |
| Revenue Model কী? | |
| Competitor কারা? (অন্তত ২টা নাম) | |
| Success কীভাবে measure হবে? | |

#### Output

```text
🎯 Business Goal : [এক লাইনে]
❌ Problem       : [User কী সমস্যায় ভুগছে?]
✅ Solution      : [আমাদের প্রজেক্ট কীভাবে সমাধান দেবে?]
👥 Audience      : [Primary User + Secondary User]
💵 Revenue Model : [Subscription / One-time / Freemium / Ads]
```

---

### 2. Competitor Research

**উদ্দেশ্য:** Market-এ কে কী করছে সেটা দেখে নিজের পজিশন ঠিক করা।

#### ন্যূনতম ৩-৫টি Competitor বিশ্লেষণ করুন

| # | Competitor Name | URL | Strength | Weakness | Opportunity |
|---|-----------------|-----|----------|----------|-------------|
| 1 | | | | | |
| 2 | | | | | |
| 3 | | | | | |

#### Design-Specific Analysis

```text
✅ Hero Section Pattern    : [কী CTA, কী Headline?]
✅ Navigation Structure    : [কী menu, কী flow?]
✅ Feature Presentation    : [Grid, List, Card?]
✅ Dashboard Layout        : [Sidebar, Topbar, Stats?]
✅ Color & Typography      : [কী color scheme?]
```

#### Output

```text
📊 Market Gap      : [কোন জায়গাটা সবাই মিস করছে?]
🚀 Differentiation : [আমাদের product কোথায় stand out করবে?]
🎨 Design Direction: [কোন competitor-এর UI inspire করবে?]
```

---

### 3. User Persona

**উদ্দেশ্য:** কার জন্য বানাচ্ছি সেটা concrete করা — assumption নয়, real profile.

```text
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
👤 PERSONA 1: [নাম]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Role       : [Student / Freelancer / Manager]
Age Range  : [18-25 / 25-40 / 40+]
Tech Level : [Beginner / Intermediate / Advanced]

🎯 Goals
  → [মূল লক্ষ্য ১]
  → [মূল লক্ষ্য ২]

😫 Pain Points
  → [সমস্যা ১]
  → [সমস্যা ২]

📱 Devices    : [Mobile / Desktop / Both]
📍 Use Context: [কোথায় ব্যবহার করবে? বাসায়? অফিসে? রাস্তায়?]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

> 📌 **রুল:** Primary persona-র জন্য design করুন, secondary persona-র জন্য accommodate করুন।

---

### 4. User Flow Design

**উদ্দেশ্য:** User কোন path-এ navigate করবে সেটা map করা।

#### Main Flow (Happy Path)

```text
[Entry Point: Google/Facebook/Search]
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

#### Edge Cases (সব প্রজেক্টের জন্য important)

```text
□ Empty State      → Dashboard-এ নতুন user কিছুই দেখবে না, তখন কী দেখাবে?
□ Error State      → API fail করলে বা ভুল input দিলে কী দেখাবে?
□ Loading State    → Skeleton loader, spinner কেমন হবে?
□ Unauthorized     → Login না করে protected page-এ গেলে কী হবে?
□ Session Expired  → Token expire হলে কী হবে?
```

---

### 5. Sitemap

**উদ্দেশ্য:** পুরো প্রজেক্টের page structure একনজরে map করা।

```text
📁 PUBLIC PAGES (সবাই দেখতে পারবে)
├── 🏠 Home         → /
├── 📄 About        → /about
├── ⭐ Features     → /features
├── 💰 Pricing      → /pricing
├── 📝 Blog         → /blog
│   └── Single Post → /blog/:slug
└── 📞 Contact      → /contact

📁 AUTH PAGES
├── 🔐 Login           → /login
├── 📝 Register        → /register
└── 🔑 Forgot Password → /forgot-password

📁 USER DASHBOARD (শুধু logged-in user)
├── 📊 Dashboard       → /dashboard
├── 👤 Profile         → /profile
├── ⚙️ Settings        → /settings
└── 📦 [Core Feature] → /[feature]

📁 ADMIN PANEL (শুধু admin role)
├── 🛡️ Admin Dashboard → /admin
├── 👥 Users           → /admin/users
├── 📝 Content         → /admin/content
└── 📈 Reports         → /admin/reports

📁 ERROR PAGES
└── ❌ 404             → *
```

> 📌 **রুল:** প্রতিটি route-এর পাশে mark করুন: 🔓 Public / 🔒 Auth / 🛡️ Admin

---

## 🎨 Phase 2: Design Track

> **ছোট প্রজেক্টের জন্য এখান থেকে সরাসরি Figma-তে যান।**

---

### 6. Page Inventory

**উদ্দেশ্য:** কতগুলো page বানাতে হবে এবং প্রতিটির priority ঠিক করা।

| Page | Route | Access | Priority |
|------|-------|--------|----------|
| Home | `/` | 🔓 Public | P1 |
| About | `/about` | 🔓 Public | P2 |
| Contact | `/contact` | 🔓 Public | P2 |
| Login | `/login` | 🔓 Public | P1 |
| Register | `/register` | 🔓 Public | P1 |
| Dashboard | `/dashboard` | 🔒 Auth | P1 |
| Profile | `/profile` | 🔒 Auth | P2 |
| Admin Panel | `/admin` | 🛡️ Admin | P2 |
| 404 | `*` | 🔓 Public | P3 |

```text
P1 = Must Have (MVP-তে লাগবেই)
P2 = Important (পরের phase-এ)
P3 = Nice to Have (সময় থাকলে)
```

---

### 7. Section Structure

**উদ্দেশ্য:** প্রতিটি page-এ কী কী section থাকবে — Figma Designer যেভাবে ভাবে।

#### 🏠 Home Page

```text
1. Navbar           → Logo, Menu Links, CTA Button
2. Hero             → Headline, Subheadline, Primary CTA, Hero Image
3. Social Proof     → "Trusted by X+ users", Logos, Ratings
4. Features         → 3-6 Feature Cards (Icon + Title + Description)
5. How It Works     → 3-Step Visual Process
6. Testimonials     → User Reviews, Photos, Names
7. Pricing          → Tier Comparison Table (যদি থাকে)
8. FAQ              → Accordion Style (5-8 Common Questions)
9. Final CTA        → Bold Background + CTA Button
10. Footer          → Logo, Links, Social Icons, Copyright
```

#### 📊 Dashboard Page

```text
1. Topbar           → Search Bar, Notifications, User Avatar Dropdown
2. Sidebar          → Navigation Menu (Collapsible)
3. Stats Overview   → 4 KPI Cards (Users, Revenue, Orders, etc.)
4. Main Content     → Core Feature-এর Table/Grid/List
5. Recent Activity  → Timeline বা Simple List
```

#### 🔐 Auth Pages (Login / Register)

```text
Option A: Split Layout
  Left Side  → Branding, Illustration, Tagline
  Right Side → Form (Email, Password, Submit Button)

Option B: Center Card Layout (Mobile-friendly)
  Center → Logo, Form, Social Login Buttons, Switch Link
```

> 📌 **রুল:** প্রতিটি section-এর পাশে লিখুন কী **data** dynamic হবে, কী **static** হবে।

---

### 8. Content Hierarchy

**উদ্দেশ্য:** User page-এ এসে প্রথমে কী দেখবে, কী action নেবে — সেটা ঠিক করা।

#### Visual Hierarchy (F-Pattern Reading)

```text
TOP-LEFT  → Most Important (Logo, Headline)
TOP-RIGHT → Secondary Action (Login, Nav CTA)
MIDDLE    → Core Content (Features, Benefits, Pricing)
BOTTOM    → Trust Signals (Testimonials, Footer, Legal)
```

#### Hero Section Priority

```text
1st 👁️  → Headline (সবচেয়ে বড়, bold)
2nd 👁️  → Subheadline (value proposition)
3rd 👁️  → Primary CTA Button (সবচেয়ে দৃশ্যমান)
4th 👁️  → Supporting Visual (Image/Illustration/Stats)
```

#### CTA Strategy

```text
🟢 Primary CTA   : "Start Free Trial" / "Get Started" → Hero + Bottom
🔵 Secondary CTA : "Watch Demo" / "Learn More"        → Hero (ছোট করে)
⚪ Inline CTA    : Feature-specific buttons            → Feature Cards
```

---

### 9. Wireframe Planning

**উদ্দেশ্য:** Figma-তে যাওয়ার আগে layout pen-paper-এ বা টুলে sketch করা।

#### Tools

| Tool | Best For | Cost |
|------|----------|------|
| **Pen + Paper** | Fastest, no friction | Free |
| **Excalidraw** | Digital sketch, clean look | Free |
| **Figma** | Directly into design | Free |
| **Relume.io** | AI-generated sitemap + wireframe | Free tier |

#### Home Page Wireframe (Text-Based)

```text
┌──────────────────────────────────────┐
│ [Logo]         [Menu] [Menu] [CTA]   │ ← Navbar
├──────────────────────────────────────┤
│ [Big Headline Text]     [Hero Image] │ ← Hero
│ [Sub-headline]                       │
│ [Primary CTA Button]                 │
├──────────────────────────────────────┤
│  "Trusted by..." [Logo] [Logo]       │ ← Social Proof
├──────────────────────────────────────┤
│ [Icon] Feature 1 [Icon] Feature 2    │ ← Features Grid
│ [Icon] Feature 3 [Icon] Feature 4    │
├──────────────────────────────────────┤
│  "What our users say..."             │ ← Testimonials
│  [Testimonial 1] [Testimonial 2]     │
├──────────────────────────────────────┤
│  [FAQ Accordion Item 1]              │ ← FAQ
│  [FAQ Accordion Item 2]              │
├──────────────────────────────────────┤
│  [Ready to start?] [Final CTA Btn]   │ ← Final CTA
├──────────────────────────────────────┤
│ [Logo] [Links] [Social] [Copyright]  │ ← Footer
└──────────────────────────────────────┘
```

#### Wireframe Checklist

```text
□ Mobile layout (max-width: 640px) ভেবে রেখেছি
□ Tablet layout (max-width: 1024px) adjust করেছি
□ Desktop layout (max-width: 1440px) ঠিক করেছি
□ Sidebar collapse behavior (mobile-এ hamburger menu)
□ Modal/Drawer position ঠিক করেছি
□ Empty state UI (যখন কোনো data থাকবে না)
□ Loading skeleton/spinner design
□ Error state (red নয়, সুন্দর illustration সহ)
```

---

### 10. Design System

**উদ্দেশ্য:** পুরো প্রজেক্ট জুড়ে consistency বজায় রাখা।

#### Step 1: Theme Selection

```text
□ Modern SaaS      → Clean, white space, bold headings
□ Corporate        → Conservative, trust-focused, blue tones
□ Minimal          → Monochrome, less elements
□ E-commerce       → Colorful, product-focused, grid-heavy
□ Dark Mode First  → Dark bg, light text
```

#### Step 2: Color Palette

```text
🎨 Primary      : #_____  → CTA Buttons, Links, Active States
🎨 Secondary    : #_____  → Supporting Elements, Hover States
🎨 Accent       : #_____  → Badges, Highlights, Sale Tags
🎨 Background   : #_____  → Main Page Background
🎨 Surface      : #_____  → Cards, Modals, Panels
🎨 Text Primary : #_____  → Headings, Important Text
🎨 Text Muted   : #_____  → Body Text, Captions, Descriptions
─────────────────────────────────────────
✅ Success      : #22c55e  → সফল Action
⚠️ Warning      : #f59e0b  → সতর্কতা
❌ Error        : #ef4444  → ভুল/সমস্যা
ℹ️ Info         : #3b82f6  → তথ্য
```

#### Step 3: Typography

```text
🔤 Heading Font : [Font Name] → Hero, Section Titles
🔤 Body Font    : [Font Name] → Paragraphs, UI Elements
🔤 Mono Font    : [Font Name] → Code Blocks, Technical Data

📏 Font Size Scale:
  xs   : 12px   (ছোট caption, helper text)
  sm   : 14px   (Secondary text, labels)
  base : 16px   (Body text, inputs)
  lg   : 18px   (Emphasized text)
  xl   : 20px   (Card titles)
  2xl  : 24px   (Section titles)
  3xl  : 30px   (Page titles)
  4xl  : 36px   (Hero subheading)
  5xl  : 48px   (Hero heading)
  6xl  : 60px   (Landing main headline)
```

#### Step 4: Spacing System

```text
📐 Base Unit: 4px

  Section Padding (top/bottom) : 80px - 120px
  Section Padding (left/right): 24px (mobile), 40px (desktop)
  Container Max-Width          : 1200px
  Card Padding                 : 24px
  Button Padding (x/y)         : 12px / 24px
  Input Padding                : 8px / 12px
  Gap Between Cards            : 24px
```

#### Step 5: Component Library

```text
⚛️ ATOMS (Base Elements)
  □ Button (Primary, Secondary, Ghost, Destructive)
  □ Input (Text, Email, Password, Number, Search)
  □ Select / Dropdown
  □ Checkbox / Radio / Toggle
  □ Badge / Tag / Label
  □ Avatar (Image + Fallback Initials)
  □ Icon (Lucide / HeroIcons)
  □ Spinner / Loader
  □ Tooltip

🧩 MOLECULES (Combined Elements)
  □ Form Field (Label + Input + Error Message)
  □ Card (Image + Title + Description + CTA)
  □ Alert / Notification (Success, Warning, Error, Info)
  □ Breadcrumb
  □ Pagination
  □ Accordion

🏗️ ORGANISMS (Complex Sections)
  □ Navbar (Logo + Menu + CTA + Mobile Hamburger)
  □ Sidebar (Collapsible, Active State)
  □ Modal / Dialog
  □ Drawer / Sheet
  □ Data Table (Sortable, Filterable)
  □ Form (Multi-step, Validation)
  □ Hero Section
  □ Footer

📄 TEMPLATES (Page Layouts)
  □ Marketing Layout (Header + Sections + Footer)
  □ Auth Layout (Centered / Split)
  □ Dashboard Layout (Sidebar + Topbar + Main Content)
  □ Admin Layout
```

---

## 🛠️ Phase 3: Development Track

> **বড় প্রজেক্টের জন্য Design Track-এর পর এগুলো করুন।**

---

### 11. Feature Breakdown (MoSCoW)

**উদ্দেশ্য:** Scope creep বন্ধ করা। কী বানাবেন, কী বানাবেন না — client-কে দেখানোর জন্য।

#### 🔴 MUST HAVE (MVP — এগুলো ছাড়া প্রজেক্ট লাইভ হবে না)

```text
□ User Registration & Login (Email + Password)
□ [Core Feature 1]
□ [Core Feature 2]
□ Basic Dashboard
□ Responsive Design
□ Essential Security (Password hashing, CSRF)
```

#### 🟡 SHOULD HAVE (v1.1 — থাকলে experience ভালো হয়)

```text
□ Social Login (Google, GitHub)
□ Email Notifications
□ Search & Filter
□ Profile Management
□ Password Reset
```

#### 🟢 NICE TO HAVE (v2 — Future, সময় বাঁচলে)

```text
□ Dark Mode
□ Multi-language Support
□ Advanced Analytics
□ File Upload
□ Export to PDF/CSV
```

#### ⚪ WON'T HAVE (এই Version-এ না)

```text
□ AI/ML Features
□ Native Mobile App
□ Real-time Chat
□ Third-party API Integrations (জটিলগুলো)
```

---

### 12. Database Schema

**উদ্দেশ্য:** Data structure আগে ঠিক করা — পরে migration headache নেই।

#### Entity Identification Rule

```text
Client-এর requirement থেকে noun গুলো বের করুন:
"Users can create projects and invite team members"
→ Entities: User, Project, Team, Invitation
```

#### Schema Template

```text
┌─────────────────────────────────────┐
│ TABLE/COLLECTION: users             │
├─────────────────────────────────────┤
│ id            : UUID / ObjectId     │
│ email         : String (unique)     │
│ password_hash : String              │
│ role          : Enum(user, admin)   │
│ name          : String              │
│ avatar_url    : String (nullable)   │
│ created_at    : Timestamp           │
│ updated_at    : Timestamp           │
└─────────────────────────────────────┘

┌─────────────────────────────────────┐
│ TABLE/COLLECTION: [entity]          │
├─────────────────────────────────────┤
│ id            : UUID / ObjectId     │
│ user_id       : FK → users.id       │
│ [field_1]     : Type                │
│ [field_2]     : Type                │
│ status        : Enum(active, draft) │
│ created_at    : Timestamp           │
│ updated_at    : Timestamp           │
└─────────────────────────────────────┘
```

#### Relationships Diagram (Quick)

```text
users   ──┬── 1:N ── orders
          │
          └── 1:N ── projects
                          │
                          └── N:M ── team_members (users)
```

---

### 13. API Planning

**উদ্দেশ্য:** Frontend-Backend contract আগেই ঠিক করা।

#### Convention

```text
Base URL   : https://api.example.com/v1
Auth       : Bearer Token (JWT) in Authorization Header
Content    : application/json
Response   : { success: boolean, data: any, message: string }
```

#### Endpoints

| Method | Endpoint | Auth | Description |
|--------|----------|------|-------------|
| **Auth** |
| POST | `/auth/register` | ❌ | User Registration |
| POST | `/auth/login` | ❌ | User Login, returns JWT |
| POST | `/auth/forgot-password` | ❌ | Send Reset Email |
| POST | `/auth/reset-password` | ❌ | Reset Password |
| GET | `/auth/me` | ✅ | Get Current User |
| **CRUD Operations** |
| GET | `/[resource]` | ✅ | List (paginated) |
| GET | `/[resource]/:id` | ✅ | Single Item |
| POST | `/[resource]` | ✅ | Create New |
| PUT | `/[resource]/:id` | ✅ | Update Existing |
| DELETE | `/[resource]/:id` | 🛡️ | Delete (Admin only) |

#### HTTP Status Codes

```text
200 → OK (Success)
201 → Created (Resource created)
400 → Bad Request (Validation error)
401 → Unauthorized (Login required)
403 → Forbidden (Permission denied)
404 → Not Found
422 → Unprocessable Entity (Business logic error)
500 → Internal Server Error
```

---

### 14. Development Roadmap

**উদ্দেশ্য:** কাজের order ঠিক করা — chaos এড়ানো।

```text
🗓️ PHASE 1 — Foundation (Week 1)
  □ Project setup (Git, Linting, Environment)
  □ Tech stack install (Next.js / Node / Express / MongoDB)
  □ Folder structure finalize
  □ Environment variables configure
  □ Authentication system (Register, Login, JWT, Middleware)
  □ Base layouts (Public Layout, Auth Layout, Dashboard Layout)

🗓️ PHASE 2 — Core UI (Week 2)
  □ All public pages UI (Home, About, Contact, Pricing)
  □ Responsive design check (Mobile, Tablet, Desktop)
  □ Reusable components build
  □ Navigation & routing complete

🗓️ PHASE 3 — Core Features (Week 3-4)
  □ [Core Feature 1] — Backend API + Frontend UI
  □ [Core Feature 2] — Backend API + Frontend UI
  □ Dashboard with real data
  □ Search, Filter, Pagination

🗓️ PHASE 4 — Supporting Features (Week 5)
  □ Profile management (Update, Avatar upload)
  □ Email notifications (SendGrid/Resend)
  □ File upload (if needed)
  □ Password reset flow

🗓️ PHASE 5 — Admin & Payment (Week 6)
  □ Admin Panel (User list, Content management, Stats)
  □ Payment Integration (Stripe / SSLCommerz)
  □ Subscription/Order management
  □ Webhook handling

🗓️ PHASE 6 — Polish & Launch (Week 7)
  □ Loading states (Skeleton, Spinner)
  □ Error states (Toasts, Error pages)
  □ Empty states (Helpful messages)
  □ SEO (Meta tags, OG images, Sitemap)
  □ Performance optimization
  □ Security audit
  □ Testing (Edge cases)
  □ Deployment (Vercel + Railway/Render/DigitalOcean)
  □ Domain + SSL setup
  □ Go Live 🚀
```

---

### 15. Deployment Checklist

```text
□ Custom domain connected
□ SSL certificate active
□ Environment variables set (Production)
□ Database backups configured
□ Error monitoring (Sentry.io)
□ Analytics (Plausible/Google Analytics)
□ Uptime monitoring (BetterStack)
□ Rate limiting enabled
□ API documentation ready
□ Client handover document created
```

---

## ✅ Pre-Development Master Checklist

```text
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
📋 PHASE 1: BUSINESS (Client Sign-off)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
□ Business goal documented
□ Target audience defined
□ Revenue model confirmed
□ Competitor research done
□ MVP scope locked (Client signed off)

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
🎨 PHASE 2: DESIGN (Ready for Figma)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
□ User personas created (min 2)
□ User flow mapped (Happy path + Edge cases)
□ Sitemap complete (All routes + Access levels)
□ Page inventory done (All pages listed)
□ Section structure defined (Per page)
□ Content hierarchy noted (Per section)
□ Wireframe sketched (At least Home, Dashboard, Auth)
□ Color palette selected
□ Typography chosen
□ Spacing system defined
□ Component list ready

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
🛠️ PHASE 3: TECHNICAL (Ready for Dev)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
□ Database schema designed
□ API endpoints listed
□ Tech stack confirmed
□ Folder structure planned
□ Environment variables documented
□ Deployment plan decided

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
✍️ PHASE 4: AGREEMENT (Client Sign-off)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
□ Requirement document sent to client
□ Timeline agreed
□ Payment terms agreed (50% advance suggested)
□ Scope clearly defined (Extra = Extra charge)
□ Contract signed (if applicable)
```

---

## 🤖 AI Mega-Prompts

### Prompt 1: Design Track Only (ছোট প্রজেক্ট)

```text
Act as a Senior Product Manager and Senior UX Designer.

Analyze the following project requirements and generate a complete
FIGMA DESIGN BLUEPRINT. Include only:

1. Business Analysis (Goal, Problem, Solution, Audience)
2. Competitor Design Research (3 competitors, analyze their UI/UX patterns)
3. User Persona (Primary user with Goals and Pain Points)
4. User Flow (Happy path + 3 edge cases)
5. Sitemap (All pages with Public/Auth/Admin labels)
6. Page Inventory (With P1/P2/P3 priority)
7. Section Structure (Every page, every section breakdown)
8. Content Hierarchy (What user sees 1st, 2nd, 3rd)
9. Wireframe Description (ASCII-style for Home, Dashboard, Auth pages)
10. Design System (Theme, 6-color palette, typography scale, components list)
11. Design Inspiration (3 reference websites with what to adopt)

Project Requirements:
[Paste Client Requirements Here]
```

### Prompt 2: Complete Project (বড় প্রজেক্ট)

```text
Act as a Senior Product Manager, UX Designer, Solution Architect,
and Senior Full-Stack Developer combined.

Analyze the following project requirements and generate a complete
PRE-DEVELOPMENT BLUEPRINT. Include all 15 sections:

1. Business Analysis (Goal, Problem, Solution, Audience, Revenue Model)
2. Competitor Analysis (5 competitors, Strengths, Weaknesses, Opportunities)
3. User Personas (2 detailed personas)
4. User Flow (Happy path + Alternative flows + Edge cases)
5. Sitemap (Full tree with access levels)
6. Page Inventory (With P1/P2/P3 priority)
7. Section Structure (Every section for every page)
8. Content Hierarchy (Visual priority per section)
9. Wireframe Description (ASCII for Home, Dashboard, Auth)
10. Design System (Theme, Colors with hex, Typography, Components)
11. Feature Breakdown (MoSCoW: Must, Should, Could, Won't)
12. Database Schema (All tables/collections with relationships)
13. API Endpoints (Method, Route, Auth, Description table)
14. Development Roadmap (Phase-by-phase, weekly breakdown)
15. MVP Scope + Future Scope (v2, v3 features)

Project Requirements:
[Paste Client Requirements Here]
```

---

## 💡 Quick Reference by Project Type

| Project Type | Key Pages | Key Sections | Core DB Entities |
|--------------|-----------|--------------|------------------|
| **SaaS/Dashboard** | Landing, Pricing, Auth, Dashboard, Settings | Stats Cards, Data Table, Charts, Sidebar | users, subscriptions, [entity] |
| **E-commerce** | Home, Category, Product, Cart, Checkout | Product Grid, Filters, Cart Drawer | users, products, categories, orders |
| **LMS/Course** | Home, Courses, Detail, Lesson, Dashboard | Course Grid, Video Player, Progress Tracker | users, courses, lessons, enrollments |
| **Portfolio/Agency** | Home, About, Portfolio, Services, Contact | Hero, Work Grid, Testimonials | projects, testimonials, messages |
| **Blog/Content** | Home, Blog List, Blog Detail, About | Article Card, Sidebar, Newsletter | users, posts, categories, comments |

---

## 🚀 Final Words

```text
┌─────────────────────────────────────────────────────┐
│                                                     │
│   🧠 Think Like a Product Manager                   │
│   🎨 Design Like a UX Designer                      │
│   🛠️ Build Like a Senior Developer                  │
│   📈 Deliver Like a Professional Freelancer         │
│                                                     │
│   ছোট প্রজেক্ট → Phase 1 + Phase 2 করুন             │
│   বড় প্রজেক্ট   → পুরো ১৫টা ধাপ করুন               │
│                                                     │
└─────────────────────────────────────────────────────┘
```

---

*Made with ❤️ for Solo Full-Stack Developers | Last Updated: 2025*



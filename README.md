# Writerly

A modern, minimal blog platform where ideas find their voice. Built as a portfolio project to demonstrate full-stack development with the latest Next.js ecosystem.

[![Next.js](https://img.shields.io/badge/Next.js-15-black?style=flat-square&logo=next.js)](https://nextjs.org)
[![TypeScript](https://img.shields.io/badge/TypeScript-5-3178C6?style=flat-square&logo=typescript&logoColor=white)](https://typescriptlang.org)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-Neon-4169E1?style=flat-square&logo=postgresql&logoColor=white)](https://www.postgresql.org)
[![Drizzle ORM](https://img.shields.io/badge/Drizzle-ORM-C5F74F?style=flat-square)](https://orm.drizzle.team)
[![Vercel](https://img.shields.io/badge/Deployed%20on-Vercel-black?style=flat-square&logo=vercel)](https://vercel.com)

🔗 **Live Demo**: [writerly-app.vercel.app](https://writerly-app.vercel.app)

---

## Screenshots

| Dashboard Page | Blog Page |
|---|---|
| ![Dashboard Page](./public/screenshots/dashboard.avif) | ![Blog Page](./public/screenshots/blog.avif) |

---

## Tech Stack

| Category | Technology |
|---|---|
| Framework | Next.js 15 (App Router) |
| Language | TypeScript |
| Styling | Tailwind CSS + shadcn/ui |
| Database | PostgreSQL (Neon) |
| ORM | Drizzle ORM |
| Auth | Better Auth |
| Validation | Zod + React Hook Form |
| Deployment | Vercel |

---

## Highlights

- Authentication with Better Auth
- PostgreSQL + Drizzle ORM
- Server Actions
- Comments system
- Protected routes

---

## Features

- **Authentication** — register, login, and logout with email & password
- **Blog Posts** — create, read, update, and delete posts
- **Comments** — leave comments on any post
- **Protected Routes** — only authenticated users can write posts
- **Author-only Actions** — edit and delete only available to post author
- **Responsive UI** — clean, minimal design that works on all devices

---

## Getting Started

### Prerequisites

- Node.js 18+
- PostgreSQL database (Neon recommended)

### Installation

1. Clone the repository

```bash
git clone https://github.com/ranzxx/writerly-app.git
cd writerly-app
```

2. Install dependencies

```bash
npm install
```

3. Set up environment variables

```bash
cp .env.example .env
```

Fill in your `.env`:

```env
BETTER_AUTH_SECRET=your_secret_here
BETTER_AUTH_URL=http://localhost:3000
DATABASE_URL=your_neon_connection_string
```

4. Push database schema

```bash
npm run db:push
```

5. Run the development server

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) to see the app.

---

## Project Structure

```
app/
├── (auth)/         → login & register pages
├── (main)/         → main app with navbar
│   ├── page.tsx    → landing page
│   └── blog/       → blog pages (list, detail, create, edit)
├── api/            → API routes
└── layout.tsx      → root layout

components/
├── shared/         → Navbar, CommentForm, AuthCard
└── ui/             → shadcn components

actions/            → Server Actions (post, comment)
lib/                → auth, db, auth-client
hooks/              → useAuth
```

---

## Challenges Solved

- Built protected routes and author-only actions using Better Auth sessions
- Implemented type-safe database operations with Drizzle ORM
- Used Server Actions for post and comment mutations
- Added form validation with Zod and React Hook Form
- Deployed a full-stack Next.js app with Neon PostgreSQL on Vercel

---

## License

MIT
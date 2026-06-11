# Prytulok — Development Context

## Product Overview

Animal shelter website that removes friction between potential adopters and the shelter. Two audiences: people who want to adopt or support the shelter, and volunteers who manage the animal database.

**Scale:** Single shelter instance, architecture ready for multi-tenant expansion.

---

## Tech Stack

- **Frontend:** Next.js (App Router) + TypeScript + Tailwind CSS
- **Backend/DB:** Supabase (PostgreSQL + Auth + Storage)
- **Email:** Resend (transactional emails for adoption applications)
- **Hosting:** Vercel

Rationale: fastest path to a working product with auth, file storage, and a relational DB included out of the box. Supabase schema can be replicated per shelter if multi-tenant is needed later.

---

## Features

### Public

| Feature | Details |
|---|---|
| Animal catalog | Filters: species (cat/dog/other), age, size, gender. Grid layout. |
| Animal card | Photo gallery, name, age, breed, size, gender, description, status badge |
| Adoption application | Form: name, phone, email, brief about yourself. Triggers email to admin + confirmation to applicant. |
| How to help | Contacts section + volunteering application form |

**Animal statuses:**
- `available` — Looking for a home
- `pending` — Has an application
- `adopted` — Found a home

### Admin Panel (authenticated, `/admin`)

| Feature | Details |
|---|---|
| Animal CRUD | Add, edit, delete animals; upload photos |
| Status management | Change animal status with one click |
| Applications list | View all adoption applications with animal reference and applicant info |

**Auth:** Single admin account (Supabase Auth). Architecture allows adding roles later (e.g., `volunteer` role with read-only applications access).

---

## Data Models

```
animals
  id, name, species, breed, age_years, age_months,
  size (small/medium/large), gender (male/female),
  description, status, photos (array), created_at

applications
  id, animal_id → animals, applicant_name, phone,
  email, message, status (new/reviewed/approved/rejected),
  created_at

volunteers
  id, name, phone, email, message, created_at
```

---

## Design System

**Tone:** Warm, homey, approachable. Think cozy editorial, not sterile SaaS.

**Palette direction:**
- Warm neutrals (cream, sand) as base
- Earthy accent (terracotta or warm amber)
- Soft greens for positive states (adopted)
- Typography: humanist sans-serif (e.g., Inter or Plus Jakarta Sans)

**Key UX principles:**
- Animal cards are the hero — photos dominate
- Status is always visible (badge on card)
- Adoption flow is max 2 steps: card → form → confirmation
- Mobile-first responsive (primary breakpoints: 375, 768, 1280)

---

## Project Constraints

- Ukrainian language only (no i18n needed)
- No online payments in v1
- Email notifications via Resend (not SMS)
- No public user accounts — applications are anonymous with contact info

---

## Commands

```bash
npm run dev        # start dev server
npm run build      # production build
npm run typecheck  # tsc --noEmit
npm run lint       # eslint
```

---

## Environment Variables

```
NEXT_PUBLIC_SUPABASE_URL=
NEXT_PUBLIC_SUPABASE_ANON_KEY=
SUPABASE_SERVICE_ROLE_KEY=
RESEND_API_KEY=
ADMIN_EMAIL=
```

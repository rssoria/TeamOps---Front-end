**WIP**

# TeamOps Frontend — SaaS Web Application

TeamOps Frontend is the **web interface** for the TeamOps platform, a multi-tenant SaaS for managing team operations, projects and tasks.

The frontend is built with **Next.js (App Router)** and focuses on **clean UI**, **secure authentication flow**, and **real-world SaaS patterns**, rather than visual complexity.

---

## 🎯 Purpose

This project was created to demonstrate:

- A production-ready **SaaS frontend architecture**
- Authentication flows integrated with an external backend API
- Protected routes and role-based navigation
- Clean UI patterns for internal tools and B2B applications
- Integration with a multi-tenant backend system

The UI is intentionally **minimal and enterprise-oriented**, prioritizing clarity and usability.

---

## 🧠 Core Concepts

### Authentication Flow

- Users authenticate against the backend API
- Refresh tokens are stored securely in **HttpOnly cookies**
- Access tokens are handled on the client side
- Routes are protected using **Next.js middleware**

### Multi-Tenant Context

- Each user belongs to a tenant (company/workspace)
- Tenant context is resolved by the backend and reflected in the UI
- The frontend never mixes data across tenants

### Role-Based UI

- Navigation and actions adapt based on user roles:
  - Owner
  - Admin
  - Member
  - Viewer

---

## 🧱 Architecture Overview

- **Framework**: Next.js (App Router)
- **Language**: TypeScript
- **Styling**: Tailwind CSS
- **UI Components**: shadcn/ui
- **State & Data Fetching**: Fetch API / React hooks
- **Auth Handling**: Next.js API Routes (BFF-style)
- **Route Protection**: Next.js Middleware

The frontend acts as a **thin client**, keeping all business rules in the backend.

---

## 📦 Main Features

- Login and logout flow
- Protected application routes
- Projects and tasks views
- Members and roles management screens
- Audit log visualization
- Clean and consistent layout (sidebar + topbar)
- Error and loading state handling

---

## 🚀 Getting Started

### Prerequisites

- Node.js (18+)
- npm or yarn
- Backend API running locally or remotely

### Environment Variables

Create a `.env.local` file:

```bash
NEXT_PUBLIC_API_URL=http://localhost:5001
```

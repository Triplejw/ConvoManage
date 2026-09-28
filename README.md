# ConvoManage

ConvoManage is a React and Supabase conference-management prototype. It focuses on the organiser workflow: authentication, a responsive dashboard, and database-backed creation and editing of conference records.

## Implemented

- Supabase email/password authentication
- Conference list, create, and update operations
- Role-aware query scaffolding for organiser, speaker, and attendee views
- Responsive React, TypeScript, and Tailwind interface
- Typed conference, session, speaker, registration, and notification data models

## Current scope

This repository is a prototype, not a complete conference SaaS product. The types and screens outline broader attendee, speaker, registration, and notification workflows, but payments, live subscriptions, production role enforcement, and end-to-end multi-tenant isolation are not implemented or verified here.

## Stack

- React 18 and TypeScript
- Vite
- Tailwind CSS
- Supabase Auth and PostgreSQL client
- Lucide React

## Local setup

```bash
git clone https://github.com/Triplejw/ConvoManage.git
cd ConvoManage
npm install
```

Create a local `.env` file with your own Supabase project values:

```bash
VITE_SUPABASE_URL=https://your-project.supabase.co
VITE_SUPABASE_ANON_KEY=your-anon-key
```

Then start the development server:

```bash
npm run dev
```

Before treating the app as production-ready, add database migrations and row-level-security policies, wire stored user roles into the auth context, and add integration tests for each role.

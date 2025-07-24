# Architectural Decisions

## ADR-001: Use Prisma ORM for Database Interactions

- **Date:** 2025-07-24
- **Status:** Accepted
- **Context:** Need a way to interact with PostgreSQL database in a type-safe manner.
- **Decision:** Use Prisma ORM for database operations.
- **Consequences:** Simplifies database queries, ensures type safety, but requires learning curve for new developers.
- **Alternatives:** Raw SQL, TypeORM.

## ADR-002: Use Vite for Frontend Build

- **Date:** 2025-07-24
- **Status:** Accepted
- **Context:** Need a fast and efficient build tool for React applications.
- **Decision:** Use Vite for building the frontend.
- **Consequences:** Faster build times, better development experience, but less mature than Create React App.
- **Alternatives:** Create React App, Next.js.
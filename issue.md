# Project Setup Plan: ElysiaJS + Drizzle + MySQL

This document outlines the high-level tasks required to initialize and set up the new backend project.

## Tech Stack
- **Runtime/Package Manager:** Bun
- **Web Framework:** ElysiaJS
- **ORM:** Drizzle ORM
- **Database:** MySQL

## High-Level Tasks

### 1. Project Initialization
- Initialize a new project using Bun in this directory.
- Install the core dependencies required for the stack (`elysia`, `drizzle-orm`, and a MySQL driver compatible with Bun/Drizzle, such as `mysql2`).
- Install essential development dependencies (e.g., `drizzle-kit` for migrations, types).

### 2. Basic Server Setup (ElysiaJS)
- Create the main application entry point (e.g., `src/index.ts`).
- Initialize a basic Elysia server instance.
- Add a simple health check endpoint (e.g., `GET /`) to verify that the server can start and accept requests.

### 3. Database Integration (Drizzle & MySQL)
- Set up a database connection module using Drizzle ORM.
- The connection should utilize environment variables for configuration (e.g., `DATABASE_URL` in a `.env` file).
- Create an initial database schema file (e.g., `src/db/schema.ts`) with a basic table definition to test the setup.
- Configure `drizzle-kit` (via `drizzle.config.ts` or similar) to manage future database migrations.

### 4. Scripts & Configuration
- Add necessary scripts to `package.json` for standard workflows:
  - Starting the development server (e.g., `bun run dev`).
  - Generating and running database migrations.

## Definition of Done
- [ ] Running `bun install` successfully installs all dependencies.
- [ ] The application starts locally without errors using the provided dev script.
- [ ] The health check endpoint is accessible and returns a success response.
- [ ] Drizzle is properly configured to communicate with a MySQL database.

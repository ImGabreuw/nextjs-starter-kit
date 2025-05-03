# 🚀 Getting Started

Welcome to the **Next.js Starter Kit**! Follow this guide to quickly set up, run, and customize your project.

---

## 1. Prerequisites

- [Node.js 18+](https://nodejs.org/) (recommended: Node 22)
- [npm](https://www.npmjs.com/) (or [pnpm](https://pnpm.io/) / [yarn](https://yarnpkg.com/))
- [Docker](https://www.docker.com/) (optional, for isolated environment)
- [Git](https://git-scm.com/)

---

## 2. Cloning the repository

```bash
git clone https://github.com/your-username/nextjs-starter-kit.git
cd nextjs-starter-kit
```

---

## 3. Installing dependencies

```bash
npm install
# or
yarn install
# or
pnpm install
```

---

## 4. Setting up environment variables

1. Copy the example file:
   ```bash
   cp .env.example .env
   ```
2. Fill in the variables in the `.env` file as needed:
   - `AUTH_SECRET`: NextAuth secret (generate with `npx auth secret`)
   - `AUTH_DISCORD_ID` and `AUTH_DISCORD_SECRET`: Discord OAuth credentials
   - `DATABASE_URL`: PostgreSQL database connection URL

> **Tip:** Check comments in `.env.example` for details on each variable.

---

## 5. Database

The project uses **Prisma ORM** and **PostgreSQL**.

- To run a local database with Docker:
  ```bash
  docker-compose up db
  ```
- To apply migrations and generate the Prisma client:
  ```bash
  npm run db:generate
  ```

---

## 6. Running the project in development

```bash
npm run dev
```

Access: [http://localhost:3000](http://localhost:3000)

---

## 7. Useful scripts

- `npm run db:studio` — Opens Prisma Studio to manage data
- `npm run db:push` — Syncs the Prisma schema with the database
- `npm run lint` — Checks for lint issues
- `npm run typecheck` — Checks TypeScript types
- `npm run build` — Builds for production

---

## 8. Docker (optional)

To run the entire stack (app + database) via Docker Compose:

```bash
docker-compose up
```

---

## 9. Deployment

The project is ready for deployment on platforms like **Vercel**, **Netlify**, or any Docker environment.

---

## 10. Questions and issues

Check the [docs/troubleshooting.md](troubleshooting.md) file for solutions to common problems.

---

## 11. Customization

- UI components are in `src/components/ui`
- Theme and layout in `src/components/layout`
- Database schema in `prisma/schema.prisma`
- Global variables and utilities in `src/lib` and `src/styles`

---

## 12. Contributing

See the instructions in [README.md](../README.md#🤝-contribute).

---

**Happy coding! 🚀**

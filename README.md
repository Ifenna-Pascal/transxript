# Transxript

Request, compile and track student transcripts online.

| Folder | What it is | Stack |
| --- | --- | --- |
| [`apps/api`](apps/api) | REST API | TypeScript, Express, MongoDB, Zod, Docker |
| [`apps/web`](apps/web) | Web app for students and admins | Next.js, TypeScript, Tailwind CSS |

## Run it locally

You need Node 18+ and MongoDB (or Docker).

```bash
# 1. API
cd apps/api
cp .env.example .env       # fill in the values
npm install
npm run dev                # http://localhost:4000

# 2. Web app (new terminal)
cd apps/web
npm install
npm run dev                # http://localhost:3000
```

The web app calls the API URL set in `apps/web/hooks/axiosHook.tsx`. Point it at `http://localhost:4000/api/` to use your local API.

This repo combines the former `transxript-api` and `transxript-web` repos, with their full commit history.

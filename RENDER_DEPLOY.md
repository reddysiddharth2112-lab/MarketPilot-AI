# MarketPilot AI — Render deployment

This project is prepared as a single Node/Express Render Web Service. The Express server serves the built React frontend and the `/api` endpoints from the same public URL.

## Render settings

- Service type: Web Service
- Runtime: Node
- Plan: Free
- Build command: `corepack enable && corepack pnpm install --frozen-lockfile && pnpm run build:render`
- Start command: `pnpm --filter @workspace/api-server run start`
- Environment variable: `SERPAPI_KEY` (set the real value in Render; never commit it)

Render automatically provides `PORT` to the running web service.

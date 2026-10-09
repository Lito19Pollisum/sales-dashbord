# Outlet performance dashboard

Vite + vanilla JS, reading from the Supabase table `public.outlet_weekly`.

## Run locally

    cp .env.example .env
    npm install
    npm run dev

## Deploy to Vercel

1. Push this folder to a Git repository and import it in Vercel (framework preset: Vite).
2. Under Settings → Environment Variables, add `VITE_SUPABASE_URL` and `VITE_SUPABASE_KEY` (values are in `.env.example`) for Production, Preview and Development.
3. Deploy. Vercel runs `npm run build` and serves `dist`.

Vite reads environment variables at build time, so redeploy after changing them.

The key is the Supabase publishable key, which is safe in browser code. The table is read-only through row-level security.

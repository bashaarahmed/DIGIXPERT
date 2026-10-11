# Contact form deployment

1. Create a Neon Postgres database. In the Neon SQL Editor, run
   `migrations/001_create_contact_messages.sql`.
2. In Vercel, set `NEON_DATABASE_URL` to the database's pooled connection string
   (with TLS enabled) for Production and any Preview/Development environments
   that need the form. Keep it server-side; do not use a `NEXT_PUBLIC_` variable.
3. Redeploy after setting the variable. Vercel installs the
   `@neondatabase/serverless` dependency from `package.json`; `/api/contact`
   accepts the form submissions.

The migration is safe to re-run on an existing database. Contact records are
stored in `contact_messages` with their submission time in `created_at`.

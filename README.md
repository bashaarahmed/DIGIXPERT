# DIGIXPERT

Portfolio site for Bashaar Ahmed, focused on full-stack development, cybersecurity, and systems programming.

## Live site

After the GitHub Pages workflow succeeds, the site will be available at <https://bashaarahmed.github.io/DIGIXPERT/>.

## Deployment

The static portfolio is deployed by the GitHub Actions workflow in `.github/workflows/pages.yml` whenever changes are pushed to `main`.

The contact form posts to `/api/contact`, which requires a serverless runtime and a Neon Postgres database. GitHub Pages only hosts static files, so form submissions will not work on the Pages site until the API is deployed separately on a platform such as Vercel and the frontend is configured to use that API. See `DEPLOYMENT.md` for backend setup.

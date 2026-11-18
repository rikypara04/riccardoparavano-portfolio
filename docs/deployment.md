# Deployment

## Target

GitHub Pages repository site owned by `rikypara04` and published under `/riccardoparavano-portfolio/`.

## Workflow

A push to `main` runs Astro validation, builds the static site, uploads the Pages artifact and deploys it to the `github-pages` environment.

## Repository setting

In GitHub, open **Settings > Pages** and set **Source** to **GitHub Actions**.

## Local validation

Run `npm run validate` before every push.
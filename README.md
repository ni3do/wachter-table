# The Wachter Table

Jonas Wachter's recipe book — live at [https://jonas-recipes.kyburz.dev](https://jonas-recipes.kyburz.dev).

This repo is a twin of [The Kyburz Table](https://github.com/ni3do/cookbook-website) (Simon's cookbook). Same stack and import sidecar; empty recipe book ready for Jonas.

## Recipes

- Markdown recipes live in `src/content/recipes/`
- Recipe images live in `public/images/recipes/`
- Add recipes by PR, or via `/api/import` when the `claude-runner` sidecar is deployed (see `docker-compose.yml` and `AGENTS.md`)

## Stack

Astro SSR + SQLite (ratings/comments) + optional Claude Code import sidecar that opens PRs against this repo.

## Local

```bash
npm install
npm run dev
```

For import flow: `cp .env.example .env`, set `GITHUB_TOKEN`, then `docker compose up --build`.

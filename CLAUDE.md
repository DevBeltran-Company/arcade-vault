# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

@AGENTS.md

## Project

Arcade Vault — plataforma para jugar online y competir por puntos (README.md). Currently a fresh `create-next-app` scaffold (App Router) with no custom features implemented yet.

## Critical: this is not stock Next.js

Per AGENTS.md, this project's `next` dependency (16.2.10) has breaking changes vs. the Next.js you were trained on — APIs, conventions, and file structure may differ. **Before writing any code that touches Next.js APIs or conventions, read the relevant guide under `node_modules/next/dist/docs/` first** (sections: `01-app`, `02-pages`, `03-architecture`, `04-community`) and follow any deprecation notices found there.

## Commands

- `npm run dev` — start dev server
- `npm run build` — production build
- `npm run start` — run production build
- `npm run lint` — ESLint (flat config, `eslint.config.mjs`, extends `eslint-config-next` core-web-vitals + typescript)

No test runner is configured yet.

## Architecture

- App Router only (`app/`), TypeScript, path alias `@/*` → repo root.
- Styling: Tailwind CSS v4 via `@tailwindcss/postcss` (no `tailwind.config` — v4 uses CSS-based config in `app/globals.css`).
- Fonts: `next/font/google` (Geist, Geist Mono) wired up in `app/layout.tsx`.

## Spec-driven workflow

README.md states this project follows spec-driven design using `/spec` and `/spec-impl` from https://github.com/Klerith/fernando-skills, installed via `npx skills@latest add Klerith/fernando-skills`. These skills are not yet installed locally — install them if asked to work with specs.

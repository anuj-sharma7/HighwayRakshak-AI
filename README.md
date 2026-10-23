# HighwayRakshak AI

**AI-assisted highway safety operations prototype** for the Highway Road Accident Prevention Innovation Challenge 2026 (Andhra Pradesh).

> **Demo only:** Segment locations, hazard alerts, condition inputs, and risk scores are simulated. No traffic cameras, weather APIs, government systems, police control rooms, or emergency services are connected. The risk indicator is a transparent weighted heuristic, not a validated accident prediction model.

## Concept

HighwayRakshak AI brings highway risk awareness into one operator workflow:
- Illustrative Andhra Pradesh corridor risk map and segment details
- Explainable risk simulator for visibility, wetness, traffic, heavy vehicles, speed exposure, road geometry, lighting and road surface
- Simulated alert feed with acknowledge, dismiss, reopen and response-task actions
- Incident/hazard reporting register
- Analytics view, evaluation metrics and phased pilot plan
- Demo scenario switching and CSV export

## Current implementation

The codebase was scaffolded in Lovable using React, TypeScript, TanStack Start/Router, Tailwind CSS, shadcn components, Lucide icons and Recharts. Browser-side demo changes use local storage. It has not yet been validated for a successful production build; fix and test any build/type errors before presenting it as a working deployment.

## Run locally

Requires Node.js (a current LTS version) and npm.

```bash
npm install
npm run dev
```

Useful checks:

```bash
npm run build
npm run test
npm run lint
```

Fix all reported errors and manually verify each route before deployment. The project is a Vite/TanStack Start app rather than a plain static site.

## Routes

- `/` — Overview
- `/risk-map` — Risk Map
- `/alerts` — Live Alerts (simulated)
- `/incidents` — Incident Reports (demo register only)
- `/simulator` — Explainable Risk Simulator
- `/analytics` — Analytics & Pilot Plan
- `/settings` — Settings & Data Sources

## Risk scoring and responsible use

The transparent demo score is a weighted sum with provisional weights: visibility (24), wetness/rain (16), traffic (16), heavy-vehicle share (10), speed exposure (16), road geometry (8), lighting (5), and surface condition (5). Scores are clamped to 0–100, with Low / Guarded / Elevated / High bands. These are demonstration assumptions only and must be calibrated against approved historical crash and exposure data before any real-world use.

An alert is an investigative/operational lead, not proof of an accident or wrongdoing. No actions are dispatched by this prototype. Any real deployment requires data governance, privacy/security review, validation, field testing, human oversight and approval from relevant authorities.

## Challenge references

See `docs/CHALLENGE_BRIEF.md` for a concise transcription of the challenge criteria and `docs/CODEX_PROMPT.md` for the repair and enhancement brief.

## Branding

**HighwayRakshak AI — Safer decisions, earlier warnings.**

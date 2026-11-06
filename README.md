# Student Internship Tracker

Students record their internship applications; advisors follow them, comment and approve offers.  
Individual project for Internet Programming I (I4-GIC, ITC, 2026–2027) by PUM BRUSMUNY (e20230959).

Current state: **Milestone M1**: Frontend prototype (Vue 3 + TypeScript, wireframes, static screens).

## Users

- **Student:** records their own applications, uploads a CV, accepts an offer after the advisor approves it
- **Advisor:** follows assigned students' applications, comments and approves offers

## Stack

- Frontend: Vue 3 + TypeScript (Vite, Vue Router, Pinia)
- Backend: NestJS 11 (REST API)
- Database: PostgreSQL with Prisma
- Testing: Vitest, Jest + Supertest

## Run the frontend prototype

Requires Node.js 22.18 or newer.

```bash
cd frontend
npm install
npm run dev
```

Open the local Vite URL (usually `http://localhost:5173`). Use the preview bar at the top to navigate between all 8 prototype views.

## Project Structure

| Path               | Purpose                                          |
| ------------------ | ------------------------------------------------ |
| `PROPOSAL.md`      | Official project proposal (Appendix A)           |
| `MILESTONES.md`    | Milestone checklists and design explanations     |
| `docs/SPEC.md`     | Functional requirements and guard table          |
| `docs/wireframes/` | UI wireframes for all 8 screens                  |
| `docs/diagrams/`   | Entity relationship diagram and status workflow  |
| `frontend/`        | Vue 3 + Vite + TypeScript application            |
| `AI_LOG.md`        | AI tool usage transparency log                   |
| `DECISIONS.md`     | Architecture and design decisions log            |

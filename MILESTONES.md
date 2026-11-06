# Project Milestones

**Project:** Student Internship Tracker  
**Student:** PUM BRUSMUNY · **ID:** e20230959  
**Repository:** https://github.com/BrusmunyPum/ip1-e20230959  
**Course:** Internet Programming I · I4-GIC · ITC · 2026–2027 · Mr. CHUN Thavorac  

---

## M0 Proposal (Week 3)

### Checklist
- [x] `PROPOSAL.md` follows the template in Appendix A
- [x] Problem stated in two sentences; target users and at least 2 roles named
- [x] 6–10 user stories, with acceptance criteria for the 3 most important (10 stories defined: 7 student, 3 advisor)
- [x] MVP scope split into must-have and nice-to-have
- [x] Entity list with main attributes and relations; at least 3 entities (User, Application, Comment)
- [x] Chosen stretch feature named (File upload: PDF CV, and Search + filter + pagination)

### Explain your design
**Question:** Which story did you cut from the MVP, and why?  
**Answer:**  
I cut the **Company Directory Management** story and **Automated Email / Push Notifications** from the MVP:
1. **Company Directory:** Instead of building a full CRUD company management system and company directory entity, `company` is kept as a validated string attribute on the `Application` entity. This avoids unnecessary relational complexity and keeps the data model lean and explainable (User, Application, Comment).
2. **Notifications:** Email and push notification delivery were omitted because they require external SMTP services and queue daemons. Instead, students and advisors see statuses and comments directly within their real-time application view and dashboards, ensuring the entire system can run self-contained and reliably via `docker compose`.

---

## M1 Frontend Prototype (Week 5)

### Checklist
- [x] Wireframes (photo or tool) of the main screens in `docs/wireframes/`
- [x] Vue 3 + TypeScript app created with Vite; strict mode on; ESLint passes
- [x] At least 4 routes / views, including a detail page with route parameters (`/applications/:id`)
- [x] At least one form with client-side validation (`ApplicationFormView.vue`)
- [x] A service layer calling mock JSON data; loading, empty and error states visible
- [x] All 8 core screens navigable via prototype preview bar

### Explain your design
**Question:** What state lives in the store and what stays inside a component? Why?  
**Answer:**  
- **Store state (Pinia):** Global application state that is shared across multiple views or needs to persist during navigation. This includes the authentication session (`auth` store with the current user, token, role), and domain data collections (`application` store) so multiple views can access the same cached dataset without duplicate network requests or losing filters when navigating between list and detail screens.
- **Component local state:** Transient UI state strictly scoped to a single component that resets when unmounted. This includes form input bindings (`v-model`), field-level validation errors (e.g., "Company is required"), dropdown toggle flags, tab selections, button loading spinners, and modal dialog visibility. Keeping UI-specific state inside the component avoids polluting the global store and maintains component reusability.

---

## M2 Backend API (Week 7)

### Checklist
- [ ] API contract (Appendix B) and ERD in `docs/`
- [ ] NestJS API with one module per resource (controller, service, DTOs)
- [ ] In-memory data; CRUD working for at least one resource
- [ ] Input validation with class-validator: 400 with a clear message on invalid body
- [ ] Consistent error responses (Appendix B)

### Explain your design
**Question:** How do you validate that an incoming request is correct before passing it to the service?  
**Answer:** *(To be answered at M2)*

---

## M3 Full-stack Integration (Week 10)

### Checklist
- [ ] PostgreSQL schema matching the ERD, managed with Prisma migrations
- [ ] Seed script (`prisma/seed.ts`) populating at least 2 entities and test data
- [ ] Frontend connects to the real backend; all M1 mock calls replaced
- [ ] Server-side search, filter or pagination working on at least one list

### Explain your design
**Question:** Walk through one network request from user click to database query and back to UI render.  
**Answer:** *(To be answered at M3)*

---

## M4 Auth and Polish (Week 12)

### Checklist
- [ ] User registration and login with bcrypt hashing and JWT
- [ ] Guards and ownership checks: users cannot access or modify another user's data
- [ ] At least 2 roles with different permissions
- [ ] Chosen stretch feature working (file upload, real-time, or scheduled task)
- [ ] Unit tests for core services (backend) and component tests (frontend)

### Explain your design
**Question:** How does the server verify that the user requesting an update owns the record?  
**Answer:** *(To be answered at M4)*

---

## M5 Production Ready (Week 14)

### Checklist
- [ ] Dockerfile and `docker-compose.yml` running the full stack with one command
- [ ] Production build passes with zero TypeScript and ESLint errors
- [ ] E2E tests for the primary user flow (Supertest)
- [ ] README (Appendix B) with architecture, setup, env variables and test accounts
- [ ] GitHub Actions workflow running tests on push

### Explain your design
**Question:** If a container crashes in production, what happens and how would you investigate it?  
**Answer:** *(To be answered at M5)*

# Decisions

- 2026-10-21: Domain is Student internship tracker, from the course list: two clear roles (student, advisor) and a real workflow
- 2026-10-21: Advisor approval is stored on the application (`approvedById`, `approvedAt`), not as a status, so the status list stays a simple forward-only line
- 2026-10-21: At most 5 active applications per student (BR-1): one clear business rule that is easy to test and to change
- 2026-10-21: Another user's application returns 404, not 403, so a student cannot learn which ids exist (IDOR protection)
- 2026-10-21: Company is a text field, not its own entity, to keep 3 entities and the scope small
- 2026-10-21: Advisor accounts come only from the seed; public registration always creates a Student, so nobody can register as an advisor
- 2026-10-25: Formally define MVP Scope (Must-have vs Nice-to-have) and stretch features (File upload and Search/filter/pagination) according to Appendix A template

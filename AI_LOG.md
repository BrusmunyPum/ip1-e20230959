# AI log

## 2026-10-21 · Proposal review
Tool: Claude Code (Claude Opus 5.5)
Asked: check PROPOSAL.md against the teacher's request (SRS-style proposal with detailed requirements)
Kept: fixed the 404 route that formatting had broken (`/:pathMatch(.*)*`); changed "reply to comments" to "add their own" in US-09
Rejected: did not adopt extra entities like Company table to keep scope small and manageable
Checked by: re-read the proposal myself before submitting

## 2026-10-25 · Milestone M0 proposal alignment
Tool: Antigravity (Gemini 3.8 Flash)
Asked: review proposal against Project Guideline.docx Appendix A template and M0 checklist
Kept: aligned PROPOSAL.md with Appendix A; condensed problem statement to two sentences; added explicit MVP Scope (Must-have vs Nice-to-have); added explicit Stretch Feature section (file upload + search/filter/pagination); created MILESTONES.md answering the design question ("Which story did you cut from the MVP, and why?")
Rejected: did not alter the established 10 user stories to maintain domain consistency
Checked by: verified all 6 checklist items in MILESTONES.md are satisfied

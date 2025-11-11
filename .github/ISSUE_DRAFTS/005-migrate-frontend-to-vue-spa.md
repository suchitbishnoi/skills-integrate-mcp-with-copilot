## Title: Improve frontend UX — migrate to small Vue SPA and add analytics placeholders

### Problem
Current frontend is a static vanilla JS page. A componentized SPA will scale better and make features like messaging and finance charts easier to integrate.

### Proposed work
- Scaffold a small Vue (or other SPA) frontend (Vue 2/3) with the key routes: Clubs, ClubPage, Activities, ActivityDetail, UserCenter.
- Include an API client wrapper and integrate auth token storage.
- Add placeholders for analytics/finance using `echarts` or simple charts.
- Provide instructions to run frontend (`yarn`/`npm`) and build static assets for FastAPI to serve or host separately.

### Acceptance criteria
- A working SPA that lists activities and clubs and can call backend endpoints.
- Build and run instructions added to `README.md`.

### Suggested labels
`enhancement`, `frontend`, `ux`, `priority:low`

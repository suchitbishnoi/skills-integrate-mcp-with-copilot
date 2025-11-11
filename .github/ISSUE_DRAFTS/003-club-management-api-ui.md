## Title: Add Club management API and basic admin UI

### Problem
The app only exposes activities; there is no concept of Clubs, club pages, or creating clubs.

### Proposed work
- Add REST endpoints: `GET /clubs`, `GET /clubs/{id}`, `POST /clubs`, `PUT /clubs/{id}`, `DELETE /clubs/{id}`.
- Add membership endpoints: join/leave club, list club members.
- Add minimal admin UI pages or API examples for creating and viewing clubs (server-rendered or SPA routes).

### Acceptance criteria
- Clubs CRUD endpoints implemented and documented.
- Frontend has a page to list clubs and view a club detail with members.

### Suggested labels
`enhancement`, `api`, `frontend`, `priority:medium`

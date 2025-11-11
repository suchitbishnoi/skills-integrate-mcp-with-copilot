## Title: Add persistent database and models for Clubs, Activities, Memberships

### Problem
Current app stores activities in-memory in `src/app.py`. Data is lost on restart and we can't support club and membership models reliably.

### Proposed work
- Add a lightweight DB (SQLite) using `SQLModel` / SQLAlchemy (or an ORM you prefer).
- Create models:
  - `Club` (id, name, description, introduce, member_count)
  - `Activity` (id, club_id, title, description, schedule, max_participants, state)
  - `Membership` (id, activity_id, user_email, role, joined_at)
- Add seed/migration script to populate the DB with the existing sample data.
- Implement a simple data access layer and unit tests for CRUD operations.

### Acceptance criteria
- App persists activities and clubs in SQLite.
- API endpoints read/write to DB and tests cover create/read/update/delete for core models.

### Suggested labels
`enhancement`, `backend`, `database`, `priority:medium`

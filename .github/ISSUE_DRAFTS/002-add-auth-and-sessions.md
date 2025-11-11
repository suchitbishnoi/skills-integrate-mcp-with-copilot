## Title: Add authentication and session management

### Problem
No authentication exists; any user can sign up/unregister without identity or permissions.

### Proposed work
- Implement a minimal auth system (email-based sign-in, or username/password) and token-based sessions (e.g., JWT) or cookie sessions.
- Protect endpoints that mutate data (signup/unregister, create activity/club, state changes).
- Add login/logout endpoints and a simple user model (email, name, role).
- Update frontend to present login form and store token or session cookie.

### Acceptance criteria
- Protected endpoints return `401` for unauthorized calls.
- Users can log in and token is accepted by backend.

### Suggested labels
`enhancement`, `auth`, `backend`, `priority:high`

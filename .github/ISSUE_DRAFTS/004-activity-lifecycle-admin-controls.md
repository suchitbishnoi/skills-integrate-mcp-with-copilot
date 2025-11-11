## Title: Implement activity lifecycle and admin controls

### Problem
Current signups are flat; there's no activity state machine (proposal → preparing → running → finished) or admin controls to advance state.

### Proposed work
- Add `state` field to Activity model (enum) and backend endpoints to move to next state (`POST /activities/{id}/advance`).
- Add role checks so only club admins or staff can advance state.
- Add UI controls for admins to see state and advance it; reflect state in activity listings.

### Acceptance criteria
- Activities have persisted state and a protected endpoint to advance state.
- UI displays state and only authorized users see advance controls.

### Suggested labels
`enhancement`, `backend`, `frontend`, `priority:medium`

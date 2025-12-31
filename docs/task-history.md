# Task History System

The history table represents immutable snapshots of change.

| Field | Meaning |
|-------|----------|
| old_status / new_status | Tracks workflow progress |
| old_priority / new_priority | Tracks urgency decisions |
| actor_id | Who performed the edit |
| created_at | When the change happened |

## When History is Recorded
- Status change
- Priority change

## Not Recorded When
- No field difference between old/new
- Soft-delete of record

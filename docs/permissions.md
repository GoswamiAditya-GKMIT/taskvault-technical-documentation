# Permissions Logic

## Access Rules
| Entity | Admin | User |
|--------|-------|------|
| User list | Full Access | Self Only |
| Task | Full Access on tasks Assigned to users and on self tasks , and view access on users self tasks | Owned or Assigned |
| Comments | Full Access | Owned or Assigned |
| Task History | Full Access | Only for owned and assigned tasks|
 
## Validation Rules
- A user cannot assign tasks
- Admin must specify an assignee if assigning
- Comments are visible only to task participants



# System Architecture

TaskVault follows a layered backend architecture:

Client → URL → DRF Views (Business Logic) → Serializers → Models → Postgres DB


## Modules Breakdown
| Module | Description |
|--------|-------------|
| `accounts` | Authentication, User, roles, permissions |
| `tasks` | Task CRUD, assignment logic, status & priority changes |
| `comments` | Adds discussion and collaboration on tasks |
| `task history` | Stores immutable audit logs |



# Database Schema

# Data Models Overview

| Entity | Purpose |
|--------|----------|
| User | Auth, roles, ownership, assignment |
| Task | Core functional entity |
| TaskHistory | Track what changed & who changed it |
| Comments | Communication on tasks |


```mermaid

erDiagram

    USERS {
        UUID id PK
        VARCHAR(150) name
        VARCHAR(255) email "UNIQUE"
        VARCHAR(128) password
        ENUM role  "admin | user"
        DATETIME created_at
        DATETIME updated_at
        DATETIME deleted_at  
    }

    TASKS {
        UUID id PK
        UUID owner_id FK    
        UUID assignee_id FK 
        VARCHAR(255) title
        TEXT description
        ENUM status "PENDING | IN_PROGRESS | COMPLETED"
        ENUM priority "HIGH | MEDIUM | LOW"
        DATETIME deadline
        DATETIME created_at
        DATETIME updated_at
        DATETIME deleted_at
    }

    TASKS_HISTORY {
        UUID id PK
        UUID task_id FK
        UUID actor_id FK
        VARCHAR(20) old_status
        VARCHAR(20) new_status
        VARCHAR(20) old_priority
        VARCHAR(20) new_priority
        DATETIME created_at
    }

    COMMENTS {
        UUID id PK
        UUID task_id FK
        UUID user_id FK
        TEXT message
        DATETIME created_at
        DATETIME updated_at
        DATETIME deleted_at
    }

    USERS ||--o{ TASKS : "owns/creates"
    USERS ||--o{ TASKS : "assigned to"
    TASKS ||--o{ TASKS_HISTORY : "audit logs"
    USERS ||--o{ TASKS_HISTORY : "changed by"
    USERS ||--o{ COMMENTS : "writes"
    TASKS ||--o{ COMMENTS : "has comments"

```
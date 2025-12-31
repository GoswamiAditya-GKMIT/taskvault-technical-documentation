# REST API Design

## Base Configuration

| Setting | Value |
|---------|--------|
| **Base URL** | `/api/v1/` |
| **API Versioning** | URI-based (e.g., `/api/v1/...`) |
| **Authentication** | JWT (Access & Refresh Tokens) |
| **Pagination** | Enabled for all list endpoints (default: 10 items per page) |
| **Update Strategy** | `PATCH` for partial updates — `PUT` is not used |

# REST API Endpoints

## Authentication
| Method | Endpoint | Description |
|--------|----------|--------------|
| POST | `/auth/register/` | Register user |
| POST | `/auth/login/` | Login & get JWT token |
| POST | `/auth/refresh/` | refresh JWT token |
| POST | `/auth/logout/` | Logout |
| GET | `/auth/rest-password/` | password reset |

---

## User Management 
| Method | Endpoint | Description |
|--------|-----------|--------------|
| GET | `/users/` | List users |
| GET | `/users/{id}/` | Get single user |
| PUT/PATCH | `/users/{id}/` | Update user details |
| DELETE | `/users/{id}/` | Soft delete task |


## Tasks
| Method | Endpoint | Description |
|--------|-----------|--------------|
| GET | `/tasks/` | List tasks (filtered by permission) |
| POST | `/tasks/` | Create task |
| GET | `/tasks/{id}/` | Get single task |
| PUT/PATCH | `/tasks/{id}/` | Update task fields |
| DELETE | `/tasks/{id}/` | Soft delete task |

---

<!-- ## Task Assignment
| Method | Endpoint |
|--------|-----------|
| PATCH | `/tasks/{id}/assign/` |

---  -->

## Comments
| Method | Endpoint |
|--------|-----------|
| POST | `/tasks/{id}/comments/` |
| GET | `/tasks/{id}/comments/` |
| GET | `/tasks/{id}/comments/{id}` |
| PUT/PATCH | `/tasks/{id}/comments/{id}` |

---

## Task History
| Method | Endpoint |
|--------|-----------|
| GET | `/tasks/{id}/history/` | View history of a task |

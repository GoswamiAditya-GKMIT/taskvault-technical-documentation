# Authentication & Roles

TaskVault uses **JWT Authentication**.

## Roles & Capabilities

| Capability | Admin | User |
|------------|-------|------|
| Create account | Yes | Yes |
| Create task for self | Yes | Yes |
| Assign tasks | Yes |  No |
| View all tasks | Yes |  No |
| Modify all tasks | Yes |  No |
| View assigned tasks | Yes | Yes |
| Modify assigned or self tasks | Yes |  Yes |
| Modify history logs | No |  No |

## Login Flow
1. POST `/api/auth/login/`
2. Receive Access + Refresh tokens
3. Include token in request header:


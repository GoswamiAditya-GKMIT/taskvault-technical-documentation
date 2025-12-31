# TaskVault - Techical Documentation

## Project Overview
TaskVault is a secure, role-based task management backend system built using **Django REST Framework** .  
It provides a structured workflow for individuals and a team to create, assign, track, and manage tasks with complete audit history and access control.

TaskVault ensures:

- Users can manage personal tasks privately.
- Admin can oversee, assign, monitor, and audit system-wide tasks.
- Every change to a task (status/priority) is recorded for accountability.

---

## Problem Statement
Many individuals and teams struggle with efficiently managing and prioritizing their tasks. Existing task management solutions often lack structured priority levels, status tracking, and secure handling of user data. There is a need for a simple, secure, and structured task manager that enables users to:

- Create, view, update, and delete tasks.
- Assign priority levels to tasks (e.g., High, Medium, Low).
- Track the status of tasks (e.g., Pending, In Progress, Completed).
- Ensure that each user's tasks are securely stored and accessible only to them.
- Clear separation between user-owned and admin-assigned tasks.
- Secure role-driven visibility and access control.
- Transparent history tracking
---

## Proposed Solution
TaskVault introduces a structured backend offering:

- **Role-based control** (admin/user)
- **JWT authentication** for secure request handling
- **Task assignment and creation logic** admin can assign taks to users, also admin and user can create tasks for themselves
- **Task Status and Priority** User and admin can set priority to an task , also update the status of tasks . 
- **Task audit history** that stores old/new values
- **Comments for collaboration** admin and user can add comment on any particular task

This creates a transparent, secure, and scalable backend that enterprises or teams can integrate with any frontend.

---

## Objectives
| Goal | Description |
|------|-------------|
| Secure Auth | Implement role-based login, JWT Auth handling |
| Task Workflow | CRUD tasks with ownership & assignment rules |
| Access Control | Users see only tasks owned or assigned to them |
| Audit Logs | Store modifications to status/priority — immutable history |
| Collaboration | Comment system for task discussions |
| PostgreSQL Focus | Stable DB design with UUID, soft delete & indexed columns |

---



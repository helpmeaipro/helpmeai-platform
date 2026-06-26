# HelpMeAI AI Workforce Table Specifications

## Module

AI Workforce

---

# Tables Covered

1. ai_employees
2. ai_departments
3. ai_roles
4. ai_skills
5. ai_memory
6. ai_tasks
7. ai_conversations
8. ai_performance
9. ai_permissions

---

# ai_employees

## Purpose

Stores all AI workforce members.

### Primary Key

ai_employee_id (UUID)

### Fields

- ai_employee_id
- name
- display_name
- role_id
- department_id
- model_provider
- model_name
- status
- version
- created_at

---

# ai_departments

### Fields

- department_id
- department_name
- description
- manager_ai_id
- created_at

---

# ai_roles

### Fields

- role_id
- role_name
- description
- permission_level
- created_at

---

# ai_skills

### Fields

- skill_id
- ai_employee_id
- skill_name
- proficiency_level
- created_at

---

# ai_memory

### Fields

- memory_id
- ai_employee_id
- memory_type
- memory_reference
- importance_score
- created_at

---

# ai_tasks

### Fields

- task_id
- ai_employee_id
- assigned_by
- task_type
- priority
- status
- created_at
- completed_at

---

# ai_conversations

### Fields

- conversation_id
- ai_employee_id
- user_id
- session_id
- message_count
- created_at

---

# ai_performance

### Fields

- performance_id
- ai_employee_id
- total_tasks
- completed_tasks
- success_rate
- average_response_time
- updated_at

---

# ai_permissions

### Fields

- permission_id
- ai_employee_id
- permission_name
- granted
- created_at

---

## Common Standards

### Foreign Keys

- ai_employee_id
- role_id
- department_id
- user_id
- session_id

---

## Security

- UUID Primary Keys
- RBAC
- Audit Logging
- Soft Delete Ready
- Enterprise Scalable

---

Status: Version 1.0

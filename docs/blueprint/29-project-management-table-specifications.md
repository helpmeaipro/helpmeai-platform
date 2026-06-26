# HelpMeAI Project Management Table Specifications

## Module

Project Management

---

# Tables Covered

1. projects
2. workspaces
3. project_members
4. tasks
5. task_comments
6. task_attachments
7. milestones
8. deliverables
9. time_entries
10. activity_logs

---

# projects

### Fields

- project_id
- project_name
- customer_id
- workspace_id
- status
- priority
- start_date
- end_date
- created_by
- created_at

---

# workspaces

### Fields

- workspace_id
- workspace_name
- owner_id
- visibility
- created_at

---

# project_members

### Fields

- member_id
- project_id
- user_id
- ai_employee_id
- role
- joined_at

---

# tasks

### Fields

- task_id
- project_id
- assigned_to
- title
- description
- priority
- status
- due_date
- completed_at

---

# task_comments

### Fields

- comment_id
- task_id
- user_id
- comment
- created_at

---

# task_attachments

### Fields

- attachment_id
- task_id
- file_id
- uploaded_by
- uploaded_at

---

# milestones

### Fields

- milestone_id
- project_id
- milestone_name
- due_date
- status

---

# deliverables

### Fields

- deliverable_id
- project_id
- deliverable_name
- status
- delivered_at

---

# time_entries

### Fields

- time_entry_id
- task_id
- user_id
- hours_logged
- entry_date

---

# activity_logs

### Fields

- activity_id
- project_id
- performed_by
- activity_type
- created_at

---

## Common Standards

### Foreign Keys

- customer_id
- workspace_id
- project_id
- user_id
- ai_employee_id
- task_id

---

## Security

- UUID Primary Keys
- RBAC
- Audit Logging
- Enterprise Scalable

---

Status: Version 1.0

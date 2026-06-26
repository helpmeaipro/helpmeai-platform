# HelpMeAI CRM Table Specifications

## Module

CRM

---

# Tables Covered

1. leads
2. contacts
3. companies
4. customers
5. deals
6. pipelines
7. pipeline_stages
8. activities
9. notes
10. follow_ups

---

# leads

### Fields

- lead_id
- full_name
- email
- phone
- source
- status
- assigned_to
- created_at

---

# contacts

### Fields

- contact_id
- company_id
- full_name
- designation
- email
- phone
- created_at

---

# companies

### Fields

- company_id
- company_name
- industry
- website
- country
- created_at

---

# customers

### Fields

- customer_id
- user_id
- company_id
- customer_since
- status
- created_at

---

# deals

### Fields

- deal_id
- customer_id
- pipeline_id
- deal_name
- value
- currency
- stage
- expected_close_date
- status

---

# pipelines

### Fields

- pipeline_id
- pipeline_name
- description
- created_at

---

# pipeline_stages

### Fields

- stage_id
- pipeline_id
- stage_name
- stage_order

---

# activities

### Fields

- activity_id
- customer_id
- activity_type
- performed_by
- activity_date
- notes

---

# notes

### Fields

- note_id
- customer_id
- created_by
- content
- created_at

---

# follow_ups

### Fields

- follow_up_id
- customer_id
- assigned_to
- follow_up_date
- status
- remarks

---

## Common Standards

### Foreign Keys

- user_id
- customer_id
- company_id
- pipeline_id

---

## Security

- UUID Primary Keys
- Audit Logging
- RBAC
- Enterprise Scalable

---

Status: Version 1.0

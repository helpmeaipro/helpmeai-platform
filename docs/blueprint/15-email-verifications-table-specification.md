# HelpMeAI Email Verifications Table Specification

## Table Name

email_verifications

---

## Description

Stores email verification requests.

---

## Primary Key

verification_id (UUID)

---

## Fields

| Field | Type | Required | Description |
|--------|------|----------|-------------|
| verification_id | UUID | Yes | Verification ID |
| user_id | UUID | Yes | User reference |
| email | String | Yes | Email address |
| verification_code | String | Yes | Verification code |
| expires_at | Timestamp | Yes | Expiration |
| verified | Boolean | Yes | Verification status |
| verified_at | Timestamp | No | Verification time |
| created_at | Timestamp | Yes | Creation time |

---

## Foreign Keys

user_id → users.user_id

---

## Indexes

- email
- verification_code
- user_id

---

## Security

- Expiry Validation
- One-Time Use
- Audit Ready

Status: Version 1.0

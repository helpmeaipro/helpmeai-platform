# HelpMeAI User Database Design

## Purpose

Store and manage all user information securely and support global scalability.

---

## Main Table

users

---

## Core Fields

- user_id (UUID)
- full_name
- username
- email
- phone
- password_hash
- profile_photo
- country
- language
- timezone
- currency
- role
- account_status
- email_verified
- phone_verified
- two_factor_enabled
- referral_code
- referred_by
- created_at
- updated_at
- last_login

---

## User Roles

- Super Admin
- Admin
- Staff
- Customer
- AI Chairman
- AI CEO
- AI PMO
- Department AI
- Worker AI

---

## Security

- UUID Primary Key
- Password Hashing
- MFA Ready
- Session Management
- Audit Logging

---

## Future Support

- Multi-Tenant
- Multi-Company
- Multi-Country
- Multi-Language

Status: Version 1.0

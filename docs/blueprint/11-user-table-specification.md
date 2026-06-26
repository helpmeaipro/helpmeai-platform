# HelpMeAI User Table Specification

## Table Name

users

---

## Description

Stores all registered users of the HelpMeAI platform.

---

## Primary Key

user_id (UUID)

---

## Fields

| Field | Type | Required | Description |
|--------|------|----------|-------------|
| user_id | UUID | Yes | Unique user identifier |
| full_name | String | Yes | Full name |
| username | String | Yes | Unique username |
| email | String | Yes | Login email |
| phone | String | Yes | Mobile number |
| password_hash | String | Yes | Encrypted password |
| profile_photo | String | No | Avatar URL |
| role | Enum | Yes | User role |
| status | Enum | Yes | Active / Suspended |
| language | String | Yes | Preferred language |
| timezone | String | Yes | User timezone |
| country | String | Yes | Country |
| currency | String | Yes | Default currency |
| referral_code | String | No | Referral code |
| referred_by | UUID | No | Referrer |
| email_verified | Boolean | Yes | Email verification |
| phone_verified | Boolean | Yes | Phone verification |
| two_factor_enabled | Boolean | Yes | MFA |
| created_at | Timestamp | Yes | Creation date |
| updated_at | Timestamp | Yes | Last update |
| last_login | Timestamp | No | Last login |

---

## Indexes

- email
- username
- phone
- referral_code

---

## Security

- UUID
- Password Hash
- MFA
- Audit Log
- Soft Delete Ready

Status: Version 1.0

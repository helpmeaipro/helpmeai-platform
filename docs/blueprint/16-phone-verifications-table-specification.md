# HelpMeAI Phone Verifications Table Specification

## Table Name

phone_verifications

---

## Description

Stores OTP verification requests for mobile numbers.

---

## Primary Key

phone_verification_id (UUID)

---

## Fields

| Field | Type | Required | Description |
|--------|------|----------|-------------|
| phone_verification_id | UUID | Yes | Verification ID |
| user_id | UUID | Yes | User reference |
| phone | String | Yes | Mobile number |
| otp_hash | String | Yes | Hashed OTP |
| expires_at | Timestamp | Yes | Expiration |
| verified | Boolean | Yes | Verification status |
| verified_at | Timestamp | No | Verification time |
| created_at | Timestamp | Yes | Creation time |

---

## Foreign Keys

user_id → users.user_id

---

## Indexes

- phone
- user_id
- expires_at

---

## Security

- Store OTP Hash
- Expiry Validation
- One-Time Use

Status: Version 1.0

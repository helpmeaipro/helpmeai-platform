# HelpMeAI Refresh Tokens Table Specification

## Table Name

refresh_tokens

---

## Description

Stores refresh tokens used to generate new access tokens securely.

---

## Primary Key

token_id (UUID)

---

## Fields

| Field | Type | Required | Description |
|--------|------|----------|-------------|
| token_id | UUID | Yes | Unique token ID |
| user_id | UUID | Yes | User reference |
| token_hash | String | Yes | Hashed refresh token |
| issued_at | Timestamp | Yes | Issue time |
| expires_at | Timestamp | Yes | Expiration |
| revoked | Boolean | Yes | Revoked status |
| revoked_at | Timestamp | No | Revocation time |
| created_at | Timestamp | Yes | Creation time |

---

## Foreign Keys

user_id → users.user_id

---

## Indexes

- user_id
- token_hash
- expires_at

---

## Security

- Store Hash Only
- Token Rotation Ready
- Revocation Ready

Status: Version 1.0

# HelpMeAI User Sessions Table Specification

## Table Name

user_sessions

---

## Description

Stores active and historical user login sessions.

---

## Primary Key

session_id (UUID)

---

## Fields

| Field | Type | Required | Description |
|--------|------|----------|-------------|
| session_id | UUID | Yes | Unique session identifier |
| user_id | UUID | Yes | User reference |
| access_token | String | Yes | JWT access token |
| refresh_token | String | Yes | Refresh token |
| ip_address | String | Yes | Login IP |
| device_name | String | Yes | Device information |
| operating_system | String | Yes | Operating system |
| browser | String | Yes | Browser |
| location | String | No | Login location |
| is_active | Boolean | Yes | Session status |
| expires_at | Timestamp | Yes | Expiration time |
| last_activity | Timestamp | Yes | Last activity |
| created_at | Timestamp | Yes | Session creation |

---

## Foreign Keys

user_id → users.user_id

---

## Indexes

- user_id
- access_token
- refresh_token
- is_active
- expires_at

---

## Security

- Token Rotation
- Session Revocation
- Device Tracking
- Audit Ready

Status: Version 1.0

# HelpMeAI Authentication Table Specifications

## Module

Authentication

---

# Tables Covered

1. password_resets
2. login_history
3. trusted_devices
4. oauth_accounts
5. api_keys

---

# password_resets

## Purpose

Stores password reset requests securely.

### Primary Key

reset_id (UUID)

### Fields

- reset_id
- user_id
- reset_token_hash
- expires_at
- used
- used_at
- created_at

### Security

- Token Hash Only
- One-Time Use
- Expiration Validation

---

# login_history

## Purpose

Stores all successful and failed login attempts.

### Primary Key

login_id (UUID)

### Fields

- login_id
- user_id
- ip_address
- device
- browser
- operating_system
- login_status
- login_method
- created_at

### Security

- Immutable Log
- Fraud Detection Ready

---

# trusted_devices

## Purpose

Stores user trusted devices for MFA.

### Primary Key

device_id (UUID)

### Fields

- device_id
- user_id
- device_name
- device_fingerprint
- trusted
- last_used
- created_at

---

# oauth_accounts

## Purpose

Stores third-party login providers.

### Primary Key

oauth_id (UUID)

### Fields

- oauth_id
- user_id
- provider
- provider_user_id
- email
- linked_at

### Supported Providers

- Google
- Microsoft
- GitHub
- Apple

---

# api_keys

## Purpose

Stores API keys for secure integrations.

### Primary Key

api_key_id (UUID)

### Fields

- api_key_id
- user_id
- api_key_hash
- permissions
- status
- expires_at
- created_at

### Security

- Hash Only
- Revocation Ready
- Permission Based

---

## Common Standards

### Foreign Key

All tables reference:

user_id → users.user_id

### Audit

- created_at
- updated_at (where applicable)

### Security

- UUID Primary Keys
- Hash Sensitive Data
- Soft Delete Ready
- Audit Logging
- Enterprise Scalable

---

Status: Version 2.0

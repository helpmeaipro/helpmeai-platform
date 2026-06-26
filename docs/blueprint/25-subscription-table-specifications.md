# HelpMeAI Subscription Table Specifications

## Module

Subscription

---

# Tables Covered

1. subscription_plans
2. user_subscriptions
3. subscription_features
4. subscription_usage
5. ai_credits
6. billing_cycles
7. subscription_history
8. enterprise_licenses

---

# subscription_plans

### Fields

- plan_id
- plan_name
- description
- monthly_price
- yearly_price
- currency
- status
- created_at

---

# user_subscriptions

### Fields

- subscription_id
- user_id
- plan_id
- start_date
- end_date
- auto_renew
- status
- created_at

---

# subscription_features

### Fields

- feature_id
- plan_id
- feature_name
- feature_value

---

# subscription_usage

### Fields

- usage_id
- subscription_id
- resource_name
- used_amount
- limit_amount
- updated_at

---

# ai_credits

### Fields

- credit_id
- user_id
- available_credits
- consumed_credits
- expires_at
- updated_at

---

# billing_cycles

### Fields

- cycle_id
- cycle_name
- duration_days

---

# subscription_history

### Fields

- history_id
- subscription_id
- action
- previous_plan
- new_plan
- changed_at

---

# enterprise_licenses

### Fields

- license_id
- organization_id
- license_key
- max_users
- expires_at
- status

---

## Common Standards

### Foreign Keys

- user_id
- plan_id
- subscription_id
- organization_id

---

## Security

- UUID Primary Keys
- Audit Logging
- Version History
- Enterprise Scalable

---

Status: Version 1.0

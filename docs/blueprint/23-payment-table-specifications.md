# HelpMeAI Payment Table Specifications

## Module

Payment

---

# Tables Covered

1. payment_transactions
2. payment_gateways
3. wallets
4. wallet_transactions
5. invoices
6. refunds
7. coupons
8. coupon_redemptions
9. taxes
10. exchange_rates

---

# payment_transactions

### Fields

- transaction_id
- user_id
- gateway_id
- invoice_id
- amount
- currency
- payment_method
- provider_transaction_id
- status
- paid_at
- created_at

---

# payment_gateways

### Fields

- gateway_id
- gateway_name
- provider
- status
- configuration_version

---

# wallets

### Fields

- wallet_id
- user_id
- balance
- currency
- updated_at

---

# wallet_transactions

### Fields

- wallet_transaction_id
- wallet_id
- transaction_type
- amount
- reference_id
- created_at

---

# invoices

### Fields

- invoice_id
- invoice_number
- user_id
- subtotal
- tax
- total
- currency
- status
- issued_at
- due_at

---

# refunds

### Fields

- refund_id
- transaction_id
- amount
- reason
- status
- processed_at

---

# coupons

### Fields

- coupon_id
- coupon_code
- discount_type
- discount_value
- valid_from
- valid_to
- usage_limit
- status

---

# coupon_redemptions

### Fields

- redemption_id
- coupon_id
- user_id
- redeemed_at

---

# taxes

### Fields

- tax_id
- country
- tax_name
- tax_rate
- effective_from

---

# exchange_rates

### Fields

- rate_id
- base_currency
- target_currency
- exchange_rate
- updated_at

---

## Common Standards

### Foreign Keys

- user_id
- gateway_id
- invoice_id
- wallet_id
- transaction_id

---

## Security

- UUID Primary Keys
- Immutable Transactions
- Audit Logging
- Multi-Currency Ready
- Enterprise Scalable

---

Status: Version 1.0

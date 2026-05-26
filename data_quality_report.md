# Data Quality Report

Generated on: 2026-05-26 22:31:13.324143

## Dataset Summary



## Dataset: customers

- Shape: (2400, 9)
- Duplicate Rows: 0

### Missing Values
- loyalty_tier: 1386
- skin_type: 401

### Column Data Types
- customer_id: object
- signup_date: object
- city_tier: object
- age_group: object
- acquisition_channel: object
- loyalty_tier: object
- preferred_category: object
- skin_type: object
- marketing_consent: object

### Invalid Value Checks

### Duplicate-like Records
- Total duplicate rows found: 0

---

## Dataset: support_tickets

- Shape: (2400, 9)
- Duplicate Rows: 0

### Missing Values
- loyalty_tier: 1386
- skin_type: 401

### Column Data Types
- customer_id: object
- signup_date: object
- city_tier: object
- age_group: object
- acquisition_channel: object
- loyalty_tier: object
- preferred_category: object
- skin_type: object
- marketing_consent: object

### Invalid Value Checks

### Duplicate-like Records
- Total duplicate rows found: 0

---

## Dataset: web_events

- Shape: (2400, 9)
- Duplicate Rows: 0

### Missing Values
- loyalty_tier: 1386
- skin_type: 401

### Column Data Types
- customer_id: object
- signup_date: object
- city_tier: object
- age_group: object
- acquisition_channel: object
- loyalty_tier: object
- preferred_category: object
- skin_type: object
- marketing_consent: object

### Invalid Value Checks

### Duplicate-like Records
- Total duplicate rows found: 0

---

## Dataset: churn_labels

- Shape: (2400, 9)
- Duplicate Rows: 0

### Missing Values
- loyalty_tier: 1386
- skin_type: 401

### Column Data Types
- customer_id: object
- signup_date: object
- city_tier: object
- age_group: object
- acquisition_channel: object
- loyalty_tier: object
- preferred_category: object
- skin_type: object
- marketing_consent: object

### Invalid Value Checks

### Duplicate-like Records
- Total duplicate rows found: 0

---

## Dataset: intervention_history

- Shape: (2400, 9)
- Duplicate Rows: 0

### Missing Values
- loyalty_tier: 1386
- skin_type: 401

### Column Data Types
- customer_id: object
- signup_date: object
- city_tier: object
- age_group: object
- acquisition_channel: object
- loyalty_tier: object
- preferred_category: object
- skin_type: object
- marketing_consent: object

### Invalid Value Checks

### Duplicate-like Records
- Total duplicate rows found: 0

---

## Join Issues Analysis

- support_tickets: 0 customer_ids not found in customers dataset
- web_events: 0 customer_ids not found in customers dataset
- churn_labels: 0 customer_ids not found in customers dataset
- intervention_history: 0 customer_ids not found in customers dataset
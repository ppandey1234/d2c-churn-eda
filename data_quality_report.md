# Data Quality Report

Generated on: 2026-05-29 01:08:17.650326

## Dataset Summary



## Dataset: customers

- Shape: (2400, 9)
- Duplicate Rows: 0

### Missing Values
- loyalty_tier: 1386
- skin_type: 401

### Column Data Types
- customer_id: str
- signup_date: str
- city_tier: str
- age_group: str
- acquisition_channel: str
- loyalty_tier: str
- preferred_category: str
- skin_type: str
- marketing_consent: str

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
- customer_id: str
- signup_date: str
- city_tier: str
- age_group: str
- acquisition_channel: str
- loyalty_tier: str
- preferred_category: str
- skin_type: str
- marketing_consent: str

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
- customer_id: str
- signup_date: str
- city_tier: str
- age_group: str
- acquisition_channel: str
- loyalty_tier: str
- preferred_category: str
- skin_type: str
- marketing_consent: str

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
- customer_id: str
- signup_date: str
- city_tier: str
- age_group: str
- acquisition_channel: str
- loyalty_tier: str
- preferred_category: str
- skin_type: str
- marketing_consent: str

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
- customer_id: str
- signup_date: str
- city_tier: str
- age_group: str
- acquisition_channel: str
- loyalty_tier: str
- preferred_category: str
- skin_type: str
- marketing_consent: str

### Invalid Value Checks

### Duplicate-like Records
- Total duplicate rows found: 0

---

## Join Issues Analysis

- support_tickets: 0 customer_ids not found in customers dataset
- web_events: 0 customer_ids not found in customers dataset
- churn_labels: 0 customer_ids not found in customers dataset
- intervention_history: 0 customer_ids not found in customers dataset
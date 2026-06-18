
# Data Quality Report

This report summarizes the data quality checks performed on the various datasets.

## 1. Duplicate Records
### 1.1 Overall Row Duplicates per DataFrame
- **CUSTOMERS DataFrame (exact row duplicates)**: 0 exact duplicate rows found.
- **ORDERS DataFrame (exact row duplicates)**: 0 exact duplicate rows found.
- **WEB DataFrame (exact row duplicates)**: 0 exact duplicate rows found.
- **LABELS DataFrame (exact row duplicates)**: 0 exact duplicate rows found.
- **INTERVENTIONS DataFrame (exact row duplicates)**: 0 exact duplicate rows found.
- **TICKETS DataFrame (exact row duplicates)**: 0 exact duplicate rows found.

### 1.2 Key ID Uniqueness Checks
- No duplicate 'customer_id' found in 'customers' table (good). All customers are unique.
- No duplicate 'order_id' found in 'orders' table (good). All order_ids are unique.
- Column 'event_id' not found in 'web' table to check for duplicates.
- Column 'intervention_id' not found in 'interventions' table to check for duplicates.
- No duplicate 'ticket_id' found in 'tickets' table (good). All ticket_ids are unique.

## 2. Missing Values

### CUSTOMERS DataFrame: Missing Values Overview
- **Columns with missing values (count and percentage):**
```
              Count  Percentage
loyalty_tier   1386       57.75
skin_type       401       16.71
```

### ORDERS DataFrame: Missing Values Overview
- **Columns with missing values (count and percentage):**
```
        Count  Percentage
rating     80         0.8
```

### WEB DataFrame: Missing Values Overview
- No missing values found in this DataFrame.

### LABELS DataFrame: Missing Values Overview
- No missing values found in this DataFrame.

### INTERVENTIONS DataFrame: Missing Values Overview
- No missing values found in this DataFrame.

### TICKETS DataFrame: Missing Values Overview
- No missing values found in this DataFrame.

## 3. Invalid or Unusual Values (Categorical/Object Columns)

### CUSTOMERS DataFrame: Categorical/Object Column Value Checks

- Column 'customer_id' has too many unique values (2400) to display value counts directly. Top 10 values shown:
```
customer_id
CUST02384    1
CUST02383    1
CUST02382    1
CUST02381    1
CUST02380    1
CUST02379    1
CUST02378    1
CUST02377    1
CUST02376    1
CUST02375    1
```

- **Column 'city_tier' value counts:**
```
city_tier
Tier 1    1005
Tier 2     870
Tier 3     525
```

- **Column 'age_group' value counts:**
```
age_group
25-34    1045
18-24     560
35-44     534
45+       261
```

- **Column 'acquisition_channel' value counts:**
```
acquisition_channel
Instagram        517
Google Search    466
Marketplace      456
Referral         396
Organic          334
Influencer       231
```

- **Column 'loyalty_tier' value counts:**
```
loyalty_tier
NaN         1386
Silver       590
Gold         319
Platinum     105
```

- **Column 'preferred_category' value counts:**
```
preferred_category
Skin Care    731
Hair Care    507
Baby Care    347
Makeup       326
Wellness     251
Fragrance    238
```

- **Column 'skin_type' value counts:**
```
skin_type
Oily           420
Dry            405
NaN            401
Sensitive      395
Combination    390
Normal         389
```

- **Column 'marketing_consent' value counts:**
```
marketing_consent
Yes    1760
No      640
```

### CUSTOMERS DataFrame: Numerical Column Outlier/Range Checks
  - No numerical columns found in CUSTOMERS to check for outliers.

### ORDERS DataFrame: Categorical/Object Column Value Checks

- Column 'order_id' has too many unique values (10009) to display value counts directly. Top 10 values shown:
```
order_id
ORD008128    1
ORD000001    1
ORD000002    1
ORD000006    1
ORD000005    1
ORD000004    1
ORD000003    1
ORD000007    1
ORD008129    1
ORD008114    1
```

- Column 'customer_id' has too many unique values (2400) to display value counts directly. Top 10 values shown:
```
customer_id
CUST02154    17
CUST00817    15
CUST00272    14
CUST01581    14
CUST01761    14
CUST00617    13
CUST01820    13
CUST01718    13
CUST00263    13
CUST00014    13
```

- **Column 'category' value counts:**
```
category
Skin Care    2700
Hair Care    2191
Makeup       1507
Baby Care    1438
Wellness     1096
Fragrance    1077
```

### ORDERS DataFrame: Numerical Column Outlier/Range Checks

- **Descriptive statistics for numerical columns:**
```
           quantity  gross_amount  discount_pct  delivery_days      returned       rating
count  10009.000000  10009.000000  10009.000000   10009.000000  10009.000000  9929.000000
mean       1.507943    743.898504      0.274121       4.454591      0.067439     3.885487
std        0.764261    600.564068      0.125525       1.769649      0.250794     1.159465
min        1.000000    149.000000      0.000000       1.000000      0.000000     1.000000
25%        1.000000    432.850000      0.190000       3.000000      0.000000     3.000000
50%        1.000000    597.060000      0.270000       4.000000      0.000000     4.000000
75%        2.000000    907.430000      0.360000       6.000000      0.000000     5.000000
max        4.000000  24789.380000      0.700000      11.000000      1.000000     5.000000
```
  - **Potential outliers detected in 'quantity'**: 247 rows (2.47%) out of 10009 total rows.
    Sample outliers:
```
     quantity
59          4
73          4
84          4
191         4
196         4
```
  - **Potential outliers detected in 'gross_amount'**: 536 rows (5.36%) out of 10009 total rows.
    Sample outliers:
```
     gross_amount
45        1781.74
73        2710.51
84        1987.35
93        2128.34
159       1908.63
```
  - **Potential outliers detected in 'discount_pct'**: 47 rows (0.47%) out of 10009 total rows.
    Sample outliers:
```
      discount_pct
1             0.64
199           0.63
860           0.62
1264          0.64
1591          0.62
```
  - **Potential outliers detected in 'delivery_days'**: 3 rows (0.03%) out of 10009 total rows.
    Sample outliers:
```
      delivery_days
797              11
7871             11
9971             11
```
  - **Potential outliers detected in 'returned'**: 675 rows (6.74%) out of 10009 total rows.
    Sample outliers:
```
    returned
1          1
21         1
32         1
91         1
92         1
```

### WEB DataFrame: Categorical/Object Column Value Checks

- Column 'customer_id' has too many unique values (2400) to display value counts directly. Top 10 values shown:
```
customer_id
CUST02384    1
CUST02383    1
CUST02382    1
CUST02381    1
CUST02380    1
CUST02379    1
CUST02378    1
CUST02377    1
CUST02376    1
CUST02375    1
```

- **Column 'snapshot_date' value counts:**
```
snapshot_date
2025-09-30    2400
```

### WEB DataFrame: Numerical Column Outlier/Range Checks

- **Descriptive statistics for numerical columns:**
```
       sessions_30d  product_views_30d  cart_adds_30d  wishlist_adds_30d  abandoned_carts_30d  email_opens_30d  campaign_clicks_30d  last_visit_days_ago
count   2400.000000        2400.000000    2400.000000        2400.000000          2400.000000      2400.000000          2400.000000          2400.000000
mean       5.460000          23.021667       1.560833           0.839167             0.672917         2.645833             0.649583            17.652500
std        4.400167          19.818043       1.644919           0.996015             0.867225         2.763346             0.951579            15.905806
min        0.000000           0.000000       0.000000           0.000000             0.000000         0.000000             0.000000             0.000000
25%        2.000000           7.000000       0.000000           0.000000             0.000000         0.000000             0.000000             4.000000
50%        5.000000          18.000000       1.000000           1.000000             0.000000         2.000000             0.000000            14.000000
75%        8.000000          34.000000       2.000000           1.000000             1.000000         5.000000             1.000000            27.000000
max       25.000000         119.000000      12.000000           6.000000             7.000000        13.000000             6.000000            60.000000
```
  - **Potential outliers detected in 'sessions_30d'**: 27 rows (1.12%) out of 2400 total rows.
    Sample outliers:
```
     sessions_30d
4              18
151            19
349            18
510            18
565            25
```
  - **Potential outliers detected in 'product_views_30d'**: 46 rows (1.92%) out of 2400 total rows.
    Sample outliers:
```
     product_views_30d
4                   95
75                  78
127                 88
151                 82
155                 77
```
  - **Potential outliers detected in 'cart_adds_30d'**: 77 rows (3.21%) out of 2400 total rows.
    Sample outliers:
```
     cart_adds_30d
75               7
92               7
127              6
219              6
229              8
```
  - **Potential outliers detected in 'wishlist_adds_30d'**: 180 rows (7.50%) out of 2400 total rows.
    Sample outliers:
```
    wishlist_adds_30d
8                   3
9                   3
24                  3
25                  3
29                  3
```
  - **Potential outliers detected in 'abandoned_carts_30d'**: 108 rows (4.50%) out of 2400 total rows.
    Sample outliers:
```
     abandoned_carts_30d
1                      3
63                     3
75                     4
92                     3
127                    4
```
  - **Potential outliers detected in 'email_opens_30d'**: 2 rows (0.08%) out of 2400 total rows.
    Sample outliers:
```
      email_opens_30d
945                13
1704               13
```
  - **Potential outliers detected in 'campaign_clicks_30d'**: 128 rows (5.33%) out of 2400 total rows.
    Sample outliers:
```
    campaign_clicks_30d
6                     3
16                    4
57                    4
81                    3
88                    3
```

### LABELS DataFrame: Categorical/Object Column Value Checks

- Column 'customer_id' has too many unique values (2400) to display value counts directly. Top 10 values shown:
```
customer_id
CUST02384    1
CUST02383    1
CUST02382    1
CUST02381    1
CUST02380    1
CUST02379    1
CUST02378    1
CUST02377    1
CUST02376    1
CUST02375    1
```

- **Column 'snapshot_date' value counts:**
```
snapshot_date
2025-09-30    2400
```

- **Column 'split' value counts:**
```
split
train         1728
validation     336
test           336
```

### LABELS DataFrame: Numerical Column Outlier/Range Checks

- **Descriptive statistics for numerical columns:**
```
       churn_next_60d
count     2400.000000
mean         0.469583
std          0.499178
min          0.000000
25%          0.000000
50%          0.000000
75%          1.000000
max          1.000000
```

### INTERVENTIONS DataFrame: Categorical/Object Column Value Checks

- Column 'customer_id' has too many unique values (2400) to display value counts directly. Top 10 values shown:
```
customer_id
CUST02384    1
CUST02383    1
CUST02382    1
CUST02381    1
CUST02380    1
CUST02379    1
CUST02378    1
CUST02377    1
CUST02376    1
CUST02375    1
```

- **Column 'snapshot_date' value counts:**
```
snapshot_date
2025-09-30    2400
```

- **Column 'last_campaign_received' value counts:**
```
last_campaign_received
none               507
new_launch         498
bundle_discount    473
free_shipping      469
welcome_offer      453
```

- **Column 'manual_priority_bucket' value counts:**
```
manual_priority_bucket
high      1163
medium     749
low        488
```

### INTERVENTIONS DataFrame: Numerical Column Outlier/Range Checks

- **Descriptive statistics for numerical columns:**
```
       last_campaign_cost
count         2400.000000
mean            18.467917
std             12.989006
min              0.000000
25%             12.000000
50%             18.000000
75%             25.000000
max             40.000000
```

### TICKETS DataFrame: Categorical/Object Column Value Checks

- Column 'ticket_id' has too many unique values (1921) to display value counts directly. Top 10 values shown:
```
ticket_id
TKT001921    1
TKT001905    1
TKT001904    1
TKT001903    1
TKT001902    1
TKT001901    1
TKT001900    1
TKT001899    1
TKT001898    1
TKT001897    1
```

- Column 'customer_id' has too many unique values (1247) to display value counts directly. Top 10 values shown:
```
customer_id
CUST00487    6
CUST00042    6
CUST00263    6
CUST01115    5
CUST01136    5
CUST01416    5
CUST01857    5
CUST00617    5
CUST01581    5
CUST00178    4
```

- **Column 'issue_type' value counts:**
```
issue_type
late_delivery       377
refund_delay        345
general_query       324
damaged_item        277
wrong_item          213
product_reaction    194
payment_issue       191
```

- **Column 'support_channel' value counts:**
```
support_channel
email    671
call     663
chat     587
```

### TICKETS DataFrame: Numerical Column Outlier/Range Checks

- **Descriptive statistics for numerical columns:**
```
       resolution_hours  sentiment_score     reopened
count       1921.000000      1921.000000  1921.000000
mean          24.789276        -0.440770     0.176991
std           14.270666         0.473244     0.381761
min            1.000000        -1.000000     0.000000
25%           14.400000        -0.890000     0.000000
50%           24.200000        -0.490000     0.000000
75%           34.600000        -0.110000     0.000000
max           74.600000         1.000000     1.000000
```
  - **Potential outliers detected in 'resolution_hours'**: 9 rows (0.47%) out of 1921 total rows.
    Sample outliers:
```
      resolution_hours
8                 74.6
231               69.0
627               67.1
1039              70.1
1064              65.9
```
  - **Warning**: Negative values found in 'sentiment_score' (check if expected).
  - **Potential outliers detected in 'reopened'**: 340 rows (17.70%) out of 1921 total rows.
    Sample outliers:
```
    reopened
4          1
16         1
25         1
28         1
31         1
```

## 4. Referential Integrity Checks (Join/Key Issues)
- **Note**: 1153 'customer_id' in 'customers' are not found in 'tickets' table. This is normal if not all customers have entries in this table (e.g., no orders, no web events).
  Sample customer_ids from 'customers' not in 'tickets': ['CUST00668', 'CUST02015', 'CUST02313', 'CUST01950', 'CUST00733']...

## 5. Date Consistency Issues

### DataFrame: CUSTOMERS

### DataFrame: ORDERS

### DataFrame: WEB

### DataFrame: LABELS

### DataFrame: INTERVENTIONS

### DataFrame: TICKETS

## 6. Columns that may cause leakage if used incorrectly
These columns should be used with caution, especially when building predictive models for churn, as they may contain information not available at the time of prediction or directly reflect the target variable.

- **List of columns potentially causing leakage if used without careful temporal consideration:**
  - **TICKETS**: resolution_hours, reopened, sentiment_score
  - **ORDERS**: delivery_date, returned
  - **INTERVENTIONS**: intervention_date, last_campaign_received, manual_priority_bucket
  - **LABELS**: churn_next_60d
  - **CUSTOMERS**: loyalty_tier

**Recommendation:** When building a churn prediction model, ensure these features are either excluded or engineered carefully to only reflect information available at the time of prediction.

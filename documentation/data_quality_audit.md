Dataset Overview
Table-Level Profile
Missing Values
Key Integrity
Foreign-Key Integrity
Duplicate Analysis
Payment Anomalies
Order Timeline Anomalies
Cleaning Decisions
Power Query Transformation Plan





• Preserve raw missing values where they are business-meaningful.
• Do not delete review rows based only on repeated review_id.
• Preserve zero-value payment records and flag them where appropriate.
• Do not overwrite anomalous dates.
• Create data-quality flags for timeline anomalies.
• Preserve the original raw CSV files unchanged.
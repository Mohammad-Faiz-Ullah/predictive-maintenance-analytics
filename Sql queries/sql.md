# SQL Analytics Queries

## Database Selection

```sql
SELECT * FROM milling_machine.predictive_maintenance;
```

---

# Total Failures

```sql
SELECT COUNT(*) AS total_failures
FROM predictive_maintenance
WHERE `Machine failure` = 1;
```
<img width="177" height="75" alt="image" src="https://github.com/user-attachments/assets/0f632345-55d3-4371-80d8-bbbeb0b034c6" />

---

# Failure Rate

```sql
SELECT ROUND(AVG(`Machine failure`) * 100, 2) AS failure_rate
FROM predictive_maintenance;
```
<img width="162" height="68" alt="image" src="https://github.com/user-attachments/assets/619cea0f-4194-4231-a499-66533303d7d4" />

---

# Average Torque During Failure

```sql
SELECT ROUND(AVG(`Torque [Nm]`), 2) AS avg_torque_failure
FROM predictive_maintenance
WHERE `Machine failure` = 1;
```
<img width="226" height="57" alt="image" src="https://github.com/user-attachments/assets/394b3c2d-0be7-4f27-b420-eca24a4530d8" />

---

# Failure by Product Type

```sql
SELECT `Type`, COUNT(*) AS failures
FROM predictive_maintenance
WHERE `Machine failure` = 1
GROUP BY `Type`;
```
<img width="191" height="128" alt="image" src="https://github.com/user-attachments/assets/85e787e0-143d-4636-befc-cc11f7b7d1bf" />

---

# Average Tool Wear Before Failure

```sql
SELECT ROUND(AVG(`Tool wear [min]`), 2) AS avg_tool_wear_failure
FROM predictive_maintenance
WHERE `Machine failure` = 1;
```
<img width="257" height="58" alt="image" src="https://github.com/user-attachments/assets/52448b17-d754-4fc4-a1d1-7786ddd90865" />

---

# High-Risk Machines

```sql
SELECT *
FROM predictive_maintenance
WHERE `Torque [Nm]` > 55
AND `Tool wear [min]` > 150;
```

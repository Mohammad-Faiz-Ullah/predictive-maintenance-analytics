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

---

# Failure Rate

```sql
SELECT ROUND(AVG(`Machine failure`) * 100, 2) AS failure_rate
FROM predictive_maintenance;
```

---

# Average Torque During Failure

```sql
SELECT ROUND(AVG(`Torque [Nm]`), 2) AS avg_torque_failure
FROM predictive_maintenance
WHERE `Machine failure` = 1;
```

---

# Failure by Product Type

```sql
SELECT `Type`, COUNT(*) AS failures
FROM predictive_maintenance
WHERE `Machine failure` = 1
GROUP BY `Type`;
```

---

# Average Tool Wear Before Failure

```sql
SELECT ROUND(AVG(`Tool wear [min]`), 2) AS avg_tool_wear_failure
FROM predictive_maintenance
WHERE `Machine failure` = 1;
```

---

# High-Risk Machines

```sql
SELECT *
FROM predictive_maintenance
WHERE `Torque [Nm]` > 55
AND `Tool wear [min]` > 150;
```

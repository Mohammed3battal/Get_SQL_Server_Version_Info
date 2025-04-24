## Script: Get_SQL_Server_Version_Info.sql

**Description**:
This script retrieves detailed information about the current SQL Server instance, including the full version string, edition, product version number, and patch level (product level).

---

### Query:
```sql
SELECT 
    @@VERSION AS SQLVersion,
    SERVERPROPERTY('Edition') AS Edition,
    SERVERPROPERTY('ProductVersion') AS ProductVersion,
    SERVERPROPERTY('ProductLevel') AS ProductLevel;
```

---

### Output Columns:

| Column           | Description                                        |
|------------------|----------------------------------------------------|
| `SQLVersion`     | Full version string including OS and build info    |
| `Edition`        | SQL Server edition (e.g., Enterprise, Standard)    |
| `ProductVersion` | Numeric version (e.g., 15.0.2000.5)                |
| `ProductLevel`   | Patch level (e.g., RTM, SP1, CU14)                 |

---

### Use Case:
- Identify SQL Server edition and version for compatibility checks
- Ensure environment meets software requirements
- Help troubleshoot issues based on patch levels
- Document SQL Server build details for audits or inventory

---



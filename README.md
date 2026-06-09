# ❄️ Talend Snowflake ETL Job

A **Talend Open Studio** data integration job that connects to a **Snowflake** database, reads category data, and logs the output — built as part of the ITI Data Engineering track.

---

## 🏗️ Job Design

The job `snowflakejob` consists of 3 components:

| Component | Type | Description |
|---|---|---|
| `tDBInput_1` | tDBInput (Snowflake) | Reads data from Snowflake database |
| `tLogRow_2` | tLogRow | Logs the fetched rows to the console |
| `tDBConnection_1` | tDBConnection | Manages the Snowflake connection |

**Flow:**
```
tDBInput_1 (Snowflake) ──► tLogRow_2
                                │
                           OnSubjobOk
                                │
                         tDBConnection_1
```

---

## 📊 Sample Output

Data read from Snowflake categories table:

```
1|Beverages|Soft drinks and coffees
2|Condiments|Sweet and savory sauces
3|Confections|Desserts and candies
4|Dairy Products|Cheeses and milk
5|Grains|Breads and cereals
6|Meat|Prepared meats
7|Produce|Dried fruit and vegetables
8|Seafood|Fish and shellfish
```

---

## 📁 Repository Structure

```
├── Job Designs/
│   ├── snowflakejob_0_1.item          # Main job definition
│   ├── snowflakejob_0_1.properties    # Job properties
│   └── snowflakejob_0_1.screenshot    # Job screenshot
├── talend.project                     # Project configuration
└── project.settings                   # Project settings
```

---

## 🛠️ Tech Stack

![Talend](https://img.shields.io/badge/Talend-Open%20Studio-FF6D00?style=for-the-badge&logo=talend&logoColor=white)
![Snowflake](https://img.shields.io/badge/Snowflake-29B5E8?style=for-the-badge&logo=snowflake&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=java&logoColor=white)

---

## ⚙️ Prerequisites

- Talend Open Studio for Data Integration
- Snowflake account with valid credentials
- Snowflake JDBC driver configured in Talend

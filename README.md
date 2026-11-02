# 📊 DataSet

Practice datasets and SQL exercises for learning data analysis.
Each dataset is a clean CSV file you can load into any database (SQL Server, MySQL, PostgreSQL) or tool (Excel, Power BI, Python/Pandas).

---

## 📁 Repository Structure

```
DataSet/
├── datasets/
│   ├── customer.csv          # E-commerce orders (1000 rows)
│   └── cricket_dataset.csv   # Player match stats (1000 rows)
└── sql/
    └── 01_sql_operators.sql  # SQL operators practice (questions + solutions)
```

---

## 🗂️ Datasets

### 1. `customer.csv` — E-commerce Orders

1000 orders placed between **Jan 2024 and Dec 2025** across 15 Indian cities.

| Column           | Type    | Description                        | Example          |
|------------------|---------|------------------------------------|------------------|
| `order_id`       | text    | Unique order ID                    | `ORD10001`       |
| `order_date`     | date    | Date of the order (YYYY-MM-DD)     | `2024-01-01`     |
| `customer_name`  | text    | Customer's full name               | `Sana Pandey`    |
| `gender`         | text    | `Male` / `Female`                  | `Female`         |
| `age`            | integer | Customer age                       | `37`             |
| `city`           | text    | Customer city                      | `Pune`           |
| `category`       | text    | Product category                   | `Fashion`        |
| `product_name`   | text    | Product purchased                  | `Women's Kurti`  |
| `quantity`       | integer | Units bought                       | `2`              |
| `unit_price`     | integer | Price per unit (₹)                 | `1819`           |
| `total_amount`   | integer | `quantity × unit_price` (₹)        | `3638`           |
| `payment_method` | text    | How the order was paid             | `UPI`            |

- **Categories:** Beauty, Books, Electronics, Fashion, Grocery, Home & Kitchen, Sports
- **Payment methods:** Cash on Delivery, Credit Card, Debit Card, Net Banking, UPI
- **Cities:** Ahmedabad, Bengaluru, Bhopal, Chandigarh, Chennai, Delhi, Hyderabad, Indore, Jaipur, Kochi, Kolkata, Lucknow, Mumbai, Patna, Pune

### 2. `cricket_dataset.csv` — Cricket Player Match Stats

1000 player performance records from international matches.

| Column          | Description                       |
|-----------------|-----------------------------------|
| `Match_ID`      | Match identifier                  |
| `Match_Date`    | Date of the match                 |
| `Player_Name`   | Player's name                     |
| `Team`          | Player's team                     |
| `Opposition`    | Opponent team                     |
| `Role`          | Batsman / Bowler / All-rounder / Wicket-keeper |
| `Format`        | ODI / T20I / Test                 |
| `Venue`         | Stadium and city                  |
| `Runs_Scored`   | Runs scored                       |
| `Balls_Faced`   | Balls faced                       |
| `Strike_Rate`   | Batting strike rate               |
| `Wickets_Taken` | Wickets taken                     |

---

## 🧑‍💻 SQL Practice

[`sql/01_sql_operators.sql`](sql/01_sql_operators.sql) — 5 questions per operator, each followed by its solution, using `customer.csv`:

| # | Operator type | Operators                         |
|---|---------------|-----------------------------------|
| 1 | Comparison    | `=` `<>` `!=` `>` `>=` `<` `<=`   |
| 2 | Logical       | `AND` `OR` `NOT`                  |
| 3 | Range         | `BETWEEN` / `NOT BETWEEN`         |
| 4 | Membership    | `IN` / `NOT IN`                   |
| 5 | Search        | `LIKE` / `NOT LIKE` (`%`, `_`)    |

### ▶️ How to run (SQL Server)

1. Clone the repo:
   ```bash
   git clone https://github.com/CodeWithMunnaX/DataSet.git
   ```
2. Open `sql/01_sql_operators.sql` in SSMS or Azure Data Studio.
3. Update the `BULK INSERT` path to where `datasets/customer.csv` is on your machine.
4. Run **STEP 0** to create the table and load the data (should return 1000 rows).
5. Try each question yourself first, then check the solution below it.

> 💡 Using MySQL or PostgreSQL? Replace `BULK INSERT` with `LOAD DATA INFILE` (MySQL) or `COPY` (PostgreSQL), and `SELECT TOP 10` with `LIMIT 10`.

---

⭐ If this helped you, give the repo a star!

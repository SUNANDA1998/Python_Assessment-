# Python_Assessment-
```
Project Title:  Monthly Bill Generator
________________________________________
### Purpose:
To automate the calculation of monthly charges for customers who use services/resources that are billed based on how long and how much they used them during a particular month.


### 🔍 Objective:

To generate monthly billing summaries from a list of items based on their active date ranges and associated rates. The system computes accurate, grouped, and pro-rata charges for resources or services provided within a specific month.

---

### 👉 Key Features:

1. **User-Defined Input:**

   * Accepts a list of billable items (`item_list`) containing:

     * Item Code
     * Quantity (qty)
     * Rate
     * Start and Stop Dates

2. **Bill Calculation Logic:**

   * Filters items that are active in the target billing month.
   * Calculates daily rate and overlap days to determine the pro-rata charge.
   * Groups charges based on:

     * `item_code`
     * `rate`
     * `billing_period` (active duration within the target month)

3. **Output Generation:**

   * Returns a dictionary with:

     * `line_items`: Grouped billing data for each active item.
     * `total_revenue`: Sum of all grouped charges.
•  Groups items with similar attributes and sums their total charge.
•  Outputs a summary bill showing:
•	Each item group
•	Quantity used
•	Billing period
•	Amount charged
________________________________________
---

### 📅 Target Month Example:

```python
result = generate_monthly_bill(item_list, "2024-11")
print(result)
```

**Sample Output:**

```python
{
  'line_items': [
    {'item_code': 'Executive Desk (4*2)', 'rate': 1000.0, 'qty': 10, 'amount': ..., 'billing_period': '2024-11-01 to 2024-10-17'},
    ...
  ],
  'total_revenue': XXXX.XX
}
```

---

### 📄 Technologies Used:

* Python (with `datetime`, `collections.defaultdict`)
* Jupyter Notebook (for development/testing)

---

### ✅ Use Cases:

* Coworking space resource billing
* Rental or subscription services
* Any item/service billing requiring prorated monthly charges

---
________________________________________


```

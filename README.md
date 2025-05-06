# Python_Assessment-
```
Project Title:  Monthly Bill Generator
________________________________________
Purpose:
   	        To automate the calculation of monthly charges for customers who use services/resources that are billed based on how long and how much they used them during a particular month.
________________________________________
Objective:
        To generate monthly billing from a list of items based on their active date ranges and associated rates. The system computes accurate, grouped, and pro-rata charges for resources or services provided within a specific month.
________________________________________
Key Features:
1.	User-Defined Input:
o	Accepts a list of billable items (item_list) containing:
	Item Code
	Quantity (qty)
	Rate
	Start and Stop Dates
2.	Bill Calculation Logic:
o	Filters items that are active in the target billing month.
o	Calculates daily rate and overlap days to determine the pro-rata charge.
o	Groups charges based on:
	item_code
	rate
	billing_period (active duration within the target month)
3.	Output Generation:
o	Returns a dictionary with:
	line_items: Grouped billing data for each active item.
	total_revenue: Sum of all grouped charges.
•  Groups items with similar attributes and sums their total charge.
•  Outputs a summary bill showing:
•	Each item group
•	Quantity used
•	Billing period
•	Amount charged
________________________________________
Target Month:
result = generate_monthly_bill(item_list, "2024-11")
print(result)

Output:

{'line_items': [{'item_code': 'Executive Desk (4*2)',
   'rate': 1080.0,
   'qty': 25,
   'amount': 27000.0,
   'billing_period': '2024-11-01 to 2024-11-30'},
  {'item_code': 'Executive Desk (4*2)',
   'rate': 1000.0,
   'qty': 5,
   'amount': 5000.0,
   'billing_period': '2024-11-01 to 2024-11-30'},
  {'item_code': 'Manager Cabin',
   'rate': 5000.0,
   'qty': 5,
   'amount': 25000.0,
   'billing_period': '2024-11-01 to 2024-11-30'},
  {'item_code': 'Parking (2S)',
   'rate': 1000.0,
   'qty': 10,
   'amount': 10000.0,
   'billing_period': '2024-11-01 to 2024-11-30'},
  {'item_code': 'Parking (2S)',
   'rate': 0.0,
   'qty': 10,
   'amount': 0.0,
   'billing_period': '2024-11-01 to 2024-11-30'},
  {'item_code': 'Executive Desk (4*2)',
   'rate': 1100.0,
   'qty': 8,
   'amount': 4693.33,
   'billing_period': '2024-11-15 to 2024-11-30'},
  {'item_code': 'Manager Cabin',
   'rate': 5200.0,
   'qty': 3,
   'amount': 5200.0,
   'billing_period': '2024-11-01 to 2024-11-10'},
  {'item_code': 'Conference Table',
   'rate': 20000.0,
   'qty': 1,
   'amount': 10666.67,
   'billing_period': '2024-11-05 to 2024-11-20'},
  {'item_code': 'Parking (2S)',
   'rate': 1000.0,
   'qty': 5,
   'amount': 2666.67,
   'billing_period': '2024-11-15 to 2024-11-30'},
  {'item_code': 'Reception Desk',
   'rate': 7000.0,
   'qty': 2,
   'amount': 14000.0,
   'billing_period': '2024-11-01 to 2024-11-30'},
  {'item_code': 'Reception Desk',
   'rate': 7000.0,
   'qty': 1,
   'amount': 3733.33,
   'billing_period': '2024-11-10 to 2024-11-25'}],
 'total_revenue': 107960.0}
________________________________________
Technologies Used:
•	Python (with datetime, collections.defaultdict)
•	Jupyter Notebook (for development/testing)
________________________________________
Use Cases:
•	Coworking space resource billing
•	Rental or subscription services
•	Any item/service billing requiring prorated monthly charges
________________________________________
```

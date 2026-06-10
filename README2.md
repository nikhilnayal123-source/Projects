Customer Journey

```text
Customer enters café
        │
        ▼
Manager assigns Table 5
        │
        ▼
Customer scans QR on Table 5
        │
        ▼
QR opens:
https://cafe.com/table/5
        │
        ▼
Customer enters:
• Name
• Contact Number
        │
        ▼
Database checks:
• Existing customer?
• Reward points?
• Loyalty discounts?
        │
        ▼
Display rewards
        │
        ▼
Customer selects menu items
        │
        ▼
Live bill updates
        │
        ▼
Customer presses Confirm Order
        │
        ▼
Order locked
        │
        ├── Database
        ├── Kitchen Screen
        └── Reception Screen
```

---

# QR Code Structure

Each table have its own QR.

Example:

| Table   | QR Opens     |
| ------- | ------------ |
| Table 1 | `.../table1` |
| Table 2 | `.../table2` |
| Table 3 | `.../table3` |


When scanned, software automatically knows:

```text
Table Number = 5
```

No need for the customer to type it.

---

# Name and Contact Page

First screen:

```text
-----------------------
    Welcome!
-----------------------

Name:
[____________]

Phone Number:
[____________]

[Check Rewards]
```

After clicking:

```text
Welcome Back, Nikhil!

Gold Member
Reward Points: 120

Available Benefits:
✓ 4% Loyalty Discount
✓ Redeem Points
☐ Save Points

[Continue Ordering]
```

---

# Menu Screen

```text
Coffee           [-] 1 [+]
Burger           [-] 2 [+]
Pizza            [-] 0 [+]

-------------------
Subtotal ₹520
Discount ₹20
Reward Used ₹50

TOTAL ₹450
-------------------

[Confirm Order]
```

The bill changes instantly.

---

# After Confirmation

Customer cannot change anything.

The database creates:

```text
CustomerID: 0012
OrderID: 20260105
Table: 5

Name: Nikhil
Phone: Stored Securely

Items:
Coffee x1
Burger x2

Discount Applied
Reward Used
Total Amount

Status: Ordered
```

---

# Kitchen Screen

```
TABLE 5

Nikhil

Coffee x1
Burger x2

[Preparing]
[Ready]
```

---

# Reception Screen

```
TABLE 5

Customer:
Nikhil

Order:
Coffee x1
Burger x2

Discount:
4%

Generate Invoice
Receive Payment
```

No phone number displayed.

---

# But here's the biggest technical question:

**How will the QR open in Python software?**

## Option 1 (Best for prototype)

QR opens a small local web page made with Python.

```
QR
 ↓
Browser
 ↓
Python Flask/FastAPI
 ↓
Database
```

Customer orders using their own phone.

This is how many real cafés work.

---

## THE PROTOTYPE

```
main.py

customer_web.py      <-- QR ordering page
kitchen_panel.py
reception_panel.py
database.py

cafe.db
```

The QR opens **customer_web.py** (running as a small web server), while the kitchen and reception use desktop panels connected to the same database.


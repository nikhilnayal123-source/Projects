# Smart Café Management & Loyalty System

## Overview

This project is a Python-based Smart Café Management System designed to automate customer ordering, kitchen workflow, billing, and customer loyalty management.

The primary objective is to reduce manual intervention, improve operational efficiency, maintain customer privacy, and build a long-term customer retention ecosystem through an integrated reward and discount system.

---

# System Workflow

## 1. Customer Arrival

* Customer enters the café.
* Manager greets the customer and assigns a table.
* Customer scans the QR Code placed on the table.

---

## 2. Customer Authentication

Before ordering, the customer is requested to enter:

* Name
* Contact Number

The system checks the central database to determine:

* Existing customer status
* Previous visit history
* Available reward points
* Loyalty tier
* Applicable discounts

### Privacy Policy

* Contact information is stored only in the main database.
* Contact information is not visible to kitchen staff.
* Contact information is not visible to reception or billing staff after authentication.
* Customer data cannot be manually edited by staff members.

---

## 3. QR-Based Ordering System

The customer can independently:

* Browse menu items
* Add or remove products
* Increase or decrease item quantities
* View real-time order cost
* View applicable discounts
* View estimated final payable amount

The ordering interface dynamically updates pricing as modifications are made.

After pressing **Confirm Order**:

* Order becomes locked.
* Customer details become non-editable.
* Order details become non-editable.
* Staff cannot modify ordered items.

---

## 4. Kitchen Management

Kitchen staff receive only the information necessary for food preparation.

Visible Information:

* Customer Name
* Ordered Items
* Item Quantities
* Order Status

Hidden Information:

* Contact Number
* Payment Information
* Reward Balance
* Invoice Details

For beverage orders, the customer's name can be used for cup labeling.

---

## 5. Reception & Billing

Reception staff can:

* View locked customer orders
* Generate invoices
* Apply taxes and service charges
* Record payment status
* Print or export bills

Reception staff cannot edit:

* Customer Name
* Contact Number
* Ordered Items
* Applied Discount Logic

The invoice is generated directly from the confirmed customer order.

---

## 6. Invoice Management

Every generated invoice is automatically stored in the central database.

Invoice records include:

* Invoice ID
* Order ID
* Customer Name
* Ordered Items
* Discounts Applied
* Taxes
* Final Amount
* Payment Method
* Date and Time

This ensures transparency and reduces the possibility of payment fraud or unauthorized bill modifications.

---

# Customer Loyalty Program

The loyalty system is designed to encourage repeat visits while allowing customers flexibility in using their rewards.

---

## A. Welcome Benefit

New customers receive a special introductory discount on their first visit.

---

## B. Visit-Based Loyalty Discount

The system rewards customers based on total previous visits.

Example:

* 2nd Visit : 1% Loyalty Discount
* 3rd Visit : 2% Loyalty Discount
* 4th Visit : 3% Loyalty Discount
* 5th Visit : 4% Loyalty Discount

The loyalty percentage increases gradually with customer engagement.

---

## C. Reward Credit Points

Customers earn reward points based on their purchases.

### Credit Point Policy

* Reward points are calculated from the final payable amount.
* 1 Reward Point = ₹1 Redemption Value.

Customers can choose to:

* Redeem available reward points.
* Save reward points for future purchases.

The system never forces point redemption.

---

## D. Monthly Loyalty Program

Customers who regularly visit throughout the month become eligible for additional benefits.

### Monthly Average Spending

Monthly Average Payment is calculated as:

m_avg_pay = (Day1 + Day2 + ... + DayN) / N

Where N represents the total number of visits during the month.

Eligible monthly customers receive:

* 50% discount on their Monthly Average Payment value.

The Monthly Average resets automatically at the end of every month.

---

## E. Yearly Loyalty Program

Customers maintaining regular monthly activity throughout the year become eligible for annual rewards.

### Eligibility

* Approximately 12–15 or more active months/periods of regular engagement.

### Annual Average Spending

y_avg_pay = (Monthly Average Payments) / Number of Eligible Months

Eligible customers receive:

* 10% discount based on their Annual Average Payment value.

---

## F. Festival Rewards

The system can provide additional promotional offers during special occasions and festivals.

Examples include:

* Diwali Offers
* Christmas Offers
* New Year Specials
* Anniversary Promotions
* Custom Seasonal Campaigns

---

# Security & Privacy Features

* Customer contact information remains private.
* Orders become immutable after confirmation.
* Staff cannot alter customer orders.
* Invoice records are permanently stored.
* Payment records are logged for auditing.
* Loyalty calculations are database-driven.
* Real-time pricing prevents billing ambiguity.

---

# System Modules

## Customer Portal

* QR Authentication
* Menu Browsing
* Real-Time Billing
* Reward Management
* Order Confirmation

## Kitchen Panel

* Order Queue
* Beverage Label Names
* Food Preparation Status

## Reception Panel

* Invoice Generation
* Tax Calculation
* Payment Processing

## Central Database

* Customer Records
* Order History
* Invoice Storage
* Loyalty Tracking
* Reward Management

---

# Future Enhancements

* Mobile Application Integration
* Online Payment Gateway
* Table Reservation System
* Inventory Management
* Sales Analytics Dashboard
* AI-Based Customer Recommendation Engine
* Staff Performance Monitoring

---

# Discount & Loyalty Terms and Conditions

1. The café reserves the right to modify or discontinue promotional offers.

2. Reward points may only be redeemed according to system policies.

3. Customers may choose to save or redeem reward points.

4. Loyalty benefits are calculated automatically by the database.

5. Monthly and yearly rewards are subject to eligibility criteria.

6. Festival discounts may not be combined with certain promotional campaigns.

7. Fraudulent or duplicate customer accounts may result in reward cancellation.

8. Customer information is stored securely and is not disclosed to staff beyond operational requirements.

9. Once an order is confirmed, customer details and ordered items cannot be modified.

10. The final discount amount is determined solely by the system's loyalty engine.

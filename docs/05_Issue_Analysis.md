# Issue Analysis

## ISSUE-001: Product Quantity Inconsistency During Order Processing

### Overview

During system testing, an inventory consistency issue was identified in the order processing workflow.

When a customer places an order for a product with limited available quantity, the system allows the order to be created without reserving the ordered quantity immediately. As a result, another customer can still view and order the same available quantity before the first order is confirmed by the administrator.

---

## Current Situation (As-Is)

The current order process:

1. Customer selects a product and enters quantity.
2. Customer adds the product to the shopping cart.
3. Customer submits an order.
4. The system creates the order with pending status.
5. Administrator reviews and confirms the order manually.

However, the product quantity remains unchanged while the order is pending.

---

## Impact Analysis

This issue may cause:

- Inconsistent product quantity information between customers and the system.
- Multiple customers placing orders for the same remaining stock.
- Administrators approving conflicting orders.
- Incorrect inventory management during order processing.

---

## Root Cause

The system does not implement an inventory reservation mechanism during the pending order stage.

Product quantity validation is performed when customers interact with the product, but the available quantity is not reserved after an order is submitted.

---

## Recommendation

Implement an inventory reservation mechanism during the checkout process.

Possible improvements:

- Reserve the ordered quantity when an order is created.
- Update available quantity displayed to other customers.
- Release reserved quantity when an order is cancelled or rejected.
- Validate product availability again before order confirmation.

---

## Priority

| Attribute | Description |
|---|---|
| Severity | High |
| Priority | High |
| Status | Open |

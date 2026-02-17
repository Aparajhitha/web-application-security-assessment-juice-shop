# 03 – Business Logic Manipulation

## Location

Basket functionality (quantity parameter manipulation)

---

## Description

During testing, basket-related parameters were manually manipulated through API interactions.

The application did not enforce strict validation on certain user-controlled inputs related to quantity and basket operations.

---

## Security Concern

Improper validation of business logic may allow:

- Quantity manipulation
- Pricing inconsistencies
- Transaction flow tampering

---

## Potential Impact

- Financial loss
- Inventory corruption
- Exploitation of transaction processes

---

## Severity
Medium

---

## Recommended Mitigation

- Implement strict server-side validation
- Validate numeric ranges and constraints
- Perform integrity checks on pricing calculations

# 04 – Insecure Direct Object Reference (IDOR) Testing

## Location

API Endpoint: /api/BasketItems

---

## Description

Direct object identifiers were tested by modifying BasketId values in API requests.

Authorization enforcement was evaluated to determine whether users could access or modify resources belonging to other users.

---

## Security Concern

If object-level authorization is not properly enforced, attackers may access or modify unauthorized resources.

---

## Potential Impact

- Unauthorized data access
- Data manipulation
- Privacy violations

---

## Severity
Low to Medium (based on observed enforcement behavior)

---

## Recommended Mitigation

- Enforce strict object-level authorization
- Validate ownership before granting access
- Avoid predictable object identifiers

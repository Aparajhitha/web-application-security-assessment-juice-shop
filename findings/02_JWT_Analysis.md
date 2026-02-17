# 02 – JWT Authentication Analysis

## Observation

The application uses JSON Web Tokens (JWT) for authentication. After login, a token is issued and stored in the browser’s localStorage.

---

## Analysis

The decoded token revealed:

- User ID
- Email address
- Role (customer)
- Password hash
- Account metadata

The token is readable on the client side and accessible via JavaScript.

---

## Security Concern

Storing JWT in localStorage exposes it to JavaScript access.

If combined with a Cross-Site Scripting (XSS) vulnerability, an attacker could retrieve the token and hijack the session.

---

## Potential Impact

- Account takeover
- Session impersonation
- Privilege misuse (if admin token is stolen)

---

## Severity
Medium (High when combined with XSS)

---

## Recommended Mitigation

- Store authentication tokens in HttpOnly secure cookies
- Avoid including sensitive information (e.g., password hashes) in JWT payload
- Implement Content Security Policy (CSP)

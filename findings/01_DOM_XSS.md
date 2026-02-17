# 01 – DOM-Based Cross-Site Scripting (XSS)

## Vulnerability Type
DOM-Based Cross-Site Scripting (XSS)

## Location
Search functionality
Route: #/search?q=

---

## Proof of Concept

### Payload Used:
<iframe src="javascript:alert('XSS')">

### Steps to Reproduce:

1. Open the application.
2. Navigate to the search bar.
3. Enter the payload above.
4. Press Enter.
5. A JavaScript alert executes inside the application.

---

## Technical Explanation

The search parameter is directly rendered into the Document Object Model (DOM) without proper sanitization or encoding.

Because the application inserts user-controlled input into the page dynamically, injected HTML and JavaScript are interpreted and executed by the browser.

This confirms the presence of a DOM-based XSS vulnerability.

---

## Security Impact

If exploited in a real-world scenario, this vulnerability could allow:

- Arbitrary JavaScript execution
- Session hijacking
- Authentication token theft
- Account takeover
- Phishing attacks within the application

---

## Severity
High

Reason: Direct execution of attacker-controlled JavaScript within the application context.

---

## Recommended Mitigation

- Sanitize and encode all user-controlled input before rendering
- Avoid unsafe DOM manipulation methods (e.g., innerHTML)
- Implement Content Security Policy (CSP)
- Store authentication tokens in HttpOnly cookies

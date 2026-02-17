Testing Approach

This assessment followed a structured black-box methodology.

1. Reconnaissance

Explored application endpoints via browser DevTools

Identified API routes via Network tab

Observed token handling in localStorage

2. Authentication Testing

Analyzed login requests

Decoded JWT tokens

Checked token storage and exposure

3. Authorization Testing

Manipulated object IDs

Tested horizontal access control

Verified ownership validation

4. Input Validation Testing

Injected JavaScript payloads in search fields

Tested DOM-based XSS vectors

Verified client-side rendering vulnerabilities

5. Business Logic Testing

Manipulated basket quantities via API

Sent negative values

Observed price manipulation behavior

Tools Used

Google Chrome DevTools

Docker

JWT.io

Manual API manipulation using fetch()

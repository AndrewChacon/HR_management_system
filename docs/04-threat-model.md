List the following for each major feature:
- Asset (whats at stake)
- Threats (what can go wrong)
- Controls (mitigation)
- Residual Risk (what remains)
- Tests (how we verify)

Some features we should model:
- Authentication
- Employee profile CRUD
- Admin role changes
- Audit logs
- Document upload

---

### 1. Authentication

Assets:
- User accounts
- Credentials (password hashes)
- Active Sessions
- Account Recovery Mechanisms

Threats:
- Brute force login attempts or credential stuffing
- User enumeration using error messages
- Account take over via weak passwords reset
- Session reuse
- Tokens leaked

Controls:
- String password hashing
- Rate limiting for endpoints such as login or password reset
- Generic authentication error messages (dont give them any hints man)
- Time limited tokens (they should expire like milk)
- Session invalidation on password changes and logging out
- Secure cookies

Tests:
- Verify error messages are all identical when authentication fails
- Test rate limiting by running a brute force attack
- Confirm that session is terminated upon user password reset
- Test and reuse expired tokens 

---

### 2. Employee profile CRUD

---

### 3. Admin role changes

---

### 4. Audit logs

---

### 5. Document upload


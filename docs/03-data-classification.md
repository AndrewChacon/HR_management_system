Create a table:
- Public: company announcements
- Internal: org chart
- Confidential: employee PII
- Restricted: SSN, bank info, salary

---

Implementing a Data Classification Strategy and Schema in Highly Regulated Industries
https://www.youtube.com/watch?v=CWbQtCac1Aw
Main points:
- impact calculus: whats the scope of the risk
- classes and controls
- discover, classify, and label 
- apply controls
- monitor and measure: having an early warning system
- audit and test: periodically do this

---

This is an extremely high level overview, a very basic data classification table for this platform

| Classification | Description                             | Examples                                              | Access Level                         | Protection Requirements                               |
| -------------- | --------------------------------------- | ----------------------------------------------------- | ------------------------------------ | ----------------------------------------------------- |
| Public         | info intended for any user              | company announcements, job titles, department names   | anyone                               | no protection needed                                  |
| Internal       | business info, not meant for the public | org chart, manager relationships, employee work email | authenticated users                  | authentication required, basic logging                |
| Confidential   | personal employee data                  | Full name, address, phone number, DOB                 | HR and Admin, limited manager access | RBAC enforced, encrypted at rest, audited access      |
| Restricted     | highly sensitive or regulated           | salary, compensation history, SSN, bank details       | Admin and strict HR access           | Strong RBAC, encryption, audit logs, minimal exposure |
- Employees should not be able to view personal data that belong to other employees
- Managers only see limited fields for direct reports
- Restricted data is never returned unless explicitly required
- Audit logs must exist for access to confidential and restricted data

---

### Trust boundaries: 
"where does data cross from least trusted to most trusted" 

Create an example simple diagram for trust boundaries

```php
User Browser -> Frontend Application -> Backend API -> Database/File Storage
```

- The user browser is fully untrusted
- Frontend is partially trusted but not enough to enforce security on its own
- Backend API will be our primary spot for enforcing trust
- Database and Storage hold the sensitive data that should never being exposed directly 
- All access control decisions happen on the server side only

---

### High risk trust boundary crossings
- Browser -> Backend API: input validation and authentication checks
- Backend -> Database: SQL injection prevention
- Admin UI -> Sensitive APIs: enforce RBAC 
- Authentication Endpoints: login, reset, invites will be required
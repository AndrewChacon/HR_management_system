# Answer these questions

- What problem does this HR system solve?
- Who are the users? (Admins, HR, Managers, Employees)
- What features will we include? (maximum of 8)
- What is out of scope? 
- What does "done" mean? 

---

# What problem does this HR system solve?

The purpose of this platform is to centralize employee records and access controlled HR workflows for a small startup. We are replacing systems like email threads, scattered spreadsheets with a single platform that supports secure on-boarding and off-boarding, role-based access, administrative audit actions to reduce the risk of data exposure as well as insider misuse

---

# Who are the users?

- Admins: system configuration and critical security actions such as managing roles, view all audit logs, and enforcing policy 
- HR: manage employee profiles, on-boarding/off-boarding, view sensitive HR fields if permitted
- Managers: view and manage reports, submit and approve requests, view team directory
- Employees: view and update limited personal profile fields, view company directory, view their own access /activity

---

# What features will we include?

1. Authentication: secure login/logout and password reset
2. RBAC Authorization: Admin, HR, Manager, Employee enforced on every route
3. Employee CRUD: create, view, update, deactivate employee records
4. Org Structure: departments and manager assignments (who reports to who)
5. On-boarding Flow: invite user -> set password -> assign role -> activate employee
6. Off-boarding Flow: disable account -> revoke sessions -> set status to terminated
7. Audit Logging: event logs for sensitive actions (role and status changes, profile edits, logins)
8. Admin Dashboard: view users and their roles, search and filter audit logs

---

# What is out of scope? 

A bunch of stuff I dont feel like doing for the prototype:
- Payroll, time tracking
- Performance reviews, PTO requests
- MFA (I do wan to implement this at some point)
- Compliance automation for SOC2
- Mobile app

---

# What does "done" mean? 

The prototype is done when:
- A user can be invited to onboard, have a role assigned and be able to log in securely
- RBAC is enforced so each role as the appropriate access for data and actions
- Admin/HR can create, update, and deactivate employee records 
- Off-boarding reliably disables accounts and revokes active sessions 
- Sensitive security actions generate audit log entries that Admins can review
- Basic security controls are implemented such as input validation, secure session handling, rate limiting on authenticated endpoints, and safe error handling
- Documentation exists for prototype contract, security charter, threat model, data classification, architecture plan
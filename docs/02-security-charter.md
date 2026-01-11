# Include:

- What are we protecting? (PII, payroll data, employment docs)
- Security goals (CIA Triad)
- Risk tolerance (What is and isnt acceptable)
- Who can do what (Proper permissions)
- Security principals that we will follow (Industry standard practices)

---

# What are we protecting?

This platform will store and process sensitive employee and organization data
The assets we will prioritize protecting include:
- Personally identifiable information: full name, address, DOB, contact info
- Employment data: role, department, manager relationships, employment status
- HR data: salary, reason for termination
- Authentication data: password hashes, reset tokens, session identifiers
- Audit logs: records of security sensitive actions and access actions

If these types of data are lost, accessed without the proper authorization, or is manipulated in some manner, could result in privacy violations, insider abuse, legal exposure, and loss of trust from our organization

---

# Security goals

Confidentiality:
- Sensitive employee and HR data is only accessible to authorized users
- Least privilege by default, enforce role based access control
- Protect credentials and session data from being leaked or reused

Integrity:
- Prevent unauthorized modification of employee records, roles, and employment status
- Audit logs should accurately reflect system activity, cannot be silently altered
- Validate all inputs to prevent logic abuse

Availability:
- System remains usable for legitimate users 
- Protect authentication and admin endpoints from being abused
- Design safe failure modes that do not expose sensitive data during errors

---

# Risk tolerance

We do not accept risks in this dojo 

Unacceptable risks:
- Any from of broken access control
- Exposure of sensitive PII or HR data to unauthorized users
- Storing plain text passwords or secrets
- Missing audit logs for security critical actions
- off-boarding failure resulting in ex-employees retaining their access

---

# Who can do what

Admins
- Manage roles and permissions
- View all employee records and audit logs
- Enforce system wide security policies
- Off-boarding and on-boarding actions

HR
- Create and update employee profiles
- View and manage sensitive HR fields
- Initiate on-boarding and off-boarding processes
- View audit logs related to HR actions

Managers
- View limited information from reports
- Update non-sensitive team related fields
- View non organizational directory

Employees
- View their own profile and employee status
- Updated limited personal information
- View non sensitive company directory info 

---

# Security principals that we will follow 

This system will be designed to follow the best security practices established for application security:
- Least privilege: users only get access required to perform their role
- Defense in depth: multiple layers of control 
- Secure by default: access should be denied unless explicitly allowed
- Fail securely: errors do not leak sensitive data, fails in a boring way
- Auditability: security critical actions are logged and made available for review
- Separation of duties: high risk actions require elevated roles
- Explicit trust boundaries: user input is always treated as untrusted
- Security as code: controls are enforced in code not just policy alone

---

Security will be treated as a core system requirement, its not a feature. This document defines the baseline expectations for protecting user data and as a guideline for security decisions related to development and operations


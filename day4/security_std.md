# Secure Design Patterns & Compliance Frameworks

## 1. Secure Design Patterns (for Apps/Systems)

Secure design patterns are architectural or coding best practices that help prevent common security issues. Think of them as "recipes" that you follow to avoid vulnerabilities.

### 🛡️ Common Secure Design Patterns

#### **Least Privilege**
- Give users/services the minimum permissions needed
- **Example**: DB user only has SELECT rights, not DROP TABLE

#### **Defense in Depth**
- Multiple layers of security (firewall → WAF → app checks → DB checks)

#### **Fail Securely**
- If something fails, it should fail safely
- **Example**: If auth service fails, block access (don't grant by default)

#### **Input Validation & Sanitization**
- Validate all user inputs to prevent SQL Injection, XSS, etc.

#### **Secure Defaults**
- Systems should start in the most secure state
- **Example**: Disable open ports by default

#### **Audit & Logging**
- Record critical actions (logins, data changes) for traceability

#### **Session Management**
- Use secure cookies, timeouts, and token-based authentication (JWT)

## 2. Key Compliance Frameworks

These are legal or industry standards that companies must follow when handling data.

### ⚖️ GDPR (General Data Protection Regulation) – Europe
- **Focus**: Personal data protection for EU citizens
- **Key Points**:
  - Users must give explicit consent to collect data
  - Users can request deletion of their data ("Right to be forgotten")
  - Data breaches must be reported within 72 hours
- **Example**: If Walmart collects EU customer emails, they must protect and allow deletion requests

### ⚖️ HIPAA (Health Insurance Portability and Accountability Act) – USA
- **Focus**: Protecting healthcare data (PHI – Protected Health Information)
- **Key Points**:
  - Encrypt patient records
  - Strict access controls (only authorized doctors/nurses can access)
  - Audit logs required for all data access
- **Example**: A hospital app storing patient lab results must be HIPAA compliant

### ⚖️ SOC 2 (Service Organization Control 2) – Global (Auditing Standard)
- **Focus**: Trust and Security of services (used for SaaS companies)
- **Built on 5 Trust Principles**:
  - Security
  - Availability
  - Processing Integrity
  - Confidentiality
  - Privacy
- **Example**: If Walmart uses a SaaS platform for order tracking, that SaaS must show SOC2 compliance to prove it handles data securely and reliably

## 🔑 Quick Comparison

| Compliance | Scope | Who Must Follow | Example |
|------------|-------|-----------------|---------|
| **GDPR** | EU citizens' personal data | Any org handling EU data | Walmart EU customer email storage |
| **HIPAA** | US healthcare data (PHI) | Hospitals, insurers, apps handling health records | Doctor's patient portal |
| **SOC 2** | SaaS platforms, cloud services | Service providers audited by customers | SaaS that Walmart uses for logistics |

## ✅ Summary

- **Secure Design Patterns** → Best practices you follow while building systems (least privilege, defense in depth, logging, etc.)
- **Compliance** → Legal/industry rules you must follow if handling sensitive data

🔹 **Compliance** = External rules you must meet  
🔹 **Secure design patterns** = Internal best practices you apply to meet those rules
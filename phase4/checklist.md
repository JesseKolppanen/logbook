✅ GDPR Compliance Checklist – Web-based Booking System (ZAP-based findings)
✅ Personal data mapping and minimization

Result	Item
⚠️	Have all personal data collected and processed in the system been identified? (Only login observed — need more inspection)
⚠️	Have you ensured that only necessary personal data is collected (data minimization)? (Cannot determine from ZAP scan alone)
⚠️	Is user age recorded to verify that the booker is over 15 years old? (Needs manual verification)
✅ User registration and management

Result	Item
❌	Does the registration form include GDPR-compliant consent for processing personal data? (ZAP scan shows login only — no evidence of consent box)
⚠️	Can users view, edit, and delete their own personal data via their account? (Not observable from ZAP)
⚠️	Is there a mechanism for the administrator to delete a reserver in accordance with the "right to be forgotten"? (Requires admin view and DB logic check)
⚠️	Is underage registration and booking restricted? (Cannot confirm — logic must be verified manually)
✅ Booking visibility

Result	Item
⚠️	Are bookings visible to non-logged-in users only at the resource level (without any personal data)? (Not visible in ZAP — check site manually)
✅	Is it ensured that names, emails, or other personal data of bookers are not exposed publicly or to unauthorized users? (ZAP did not find leaks — good sign)
✅ Access control and authorization

Result	Item
⚠️	Have you ensured that only administrators can add, modify, and delete resources and bookings? (Authorization not tested in ZAP — manual check needed)
⚠️	Is the system using role-based access control (e.g., reserver vs. administrator)? (Needs login and role check)
⚠️	Are administrator privileges limited to ensure GDPR compliance? (Not testable via ZAP scan — business logic check needed)
✅ Privacy by Design Principles

Result	Item
⚠️	Has Privacy by Default been implemented? (Requires code/database review)
⚠️	Are logs implemented without unnecessarily storing personal data? (Not visible in ZAP — backend check required)
✅	Are forms and system components designed with data protection in mind? (ZAP scan found login only — no security flaws like data leaks)
✅ Data security

Result	Item
✅	Are CSRF, XSS, and SQL injection protections implemented? (ZAP did not detect any common vulnerabilities — good sign)
⚠️	Are passwords securely hashed using a strong algorithm? (ZAP cannot check this — check backend code or DB directly)
⚠️	Are data backup and recovery processes GDPR-compliant? (Out of scope for ZAP — organizational control)
⚠️	Is personal data stored in data centers located within the EU? (Needs infrastructure review — not testable by ZAP)
✅ Data anonymization and pseudonymization

Result	Item
⚠️	Is personal data anonymized where possible? (Not evident — DB logic check required)
⚠️	Are pseudonymization techniques used to protect data? (Backend logic must be inspected)
✅ Data subject rights

Result	Item
⚠️	Can users download or request all personal data related to them? (No export interface observed in ZAP)
⚠️	Is there a process to request deletion of personal data? (Check account deletion / admin controls)
⚠️	Can users withdraw consent for data processing? (Consent not even observed yet — needs implementation)
✅ Documentation and communication

Result	Item
❌	Is there a privacy policy available during registration and easily accessible? (You mentioned this is missing)
⚠️	Are devs/admins provided with documented data protection practices? (Check GitHub or company docs)
❌	Is there a documented data breach response process? (Not observed — could be added to README or policy)
✅ Summary

    ✅ Positive: No critical vulnerabilities found by ZAP; no personal data exposed in unauthenticated areas.

    ❌ Missing: Privacy policy, user consent for data processing, and breach response documentation.

    ⚠️ Attention Needed: Many areas require manual verification or code review, including age checks, consent handling, data minimization, and pseudonymization.

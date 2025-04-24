# ✅ GDPR Compliance Checklist – Web-based Booking System

## 🔍 Personal Data Mapping and Minimization
- [ ] Have all personal data collected and processed in the system been identified? *(⚠️ ZAP shows login, but full scope unknown)*
- [ ] Have you ensured that only necessary personal data is collected (data minimization)? *(⚠️ Manual check required)*
- [ ] Is user age recorded to verify that the booker is over 15 years old? *(⚠️ Logic not verified)*

## 👤 User Registration and Management
- [ ] Does the registration form include GDPR-compliant consent for processing personal data? *(❌ No evidence found in ZAP)*
- [ ] Can users view, edit, and delete their own personal data via their account? *(⚠️ Unknown)*
- [ ] Is there a mechanism for the administrator to delete a reserver ("right to be forgotten")? *(⚠️ Manual validation needed)*
- [ ] Is underage registration and booking functionality restricted? *(⚠️ Logic unverified)*

## 📅 Booking Visibility
- [ ] Are bookings visible to non-logged-in users only at the resource level (without personal data)? *(⚠️ Needs UI check)*
- [x] Is it ensured that names, emails, or other personal data of bookers are not exposed publicly or to unauthorized users? *(✅ ZAP scan shows no leaks)*

## 🔐 Access Control and Authorization
- [ ] Have you ensured that only administrators can add, modify, and delete resources and bookings? *(⚠️ Needs role logic check)*
- [ ] Is the system using role-based access control (e.g., reserver vs. administrator)? *(⚠️ Not confirmed)*
- [ ] Are administrator privileges limited to ensure GDPR compliance? *(⚠️ Backend logic unknown)*

## 🛠 Privacy by Design Principles
- [ ] Has Privacy by Default been implemented (e.g., minimal data collected by default)? *(⚠️ Needs confirmation)*
- [ ] Are logs implemented without unnecessarily storing personal data? *(⚠️ Backend config required)*
- [x] Are forms and system components designed with data protection in mind? *(✅ No critical issues found by ZAP)*

## 🔒 Data Security
- [x] Are CSRF, XSS, and SQL injection protections implemented? *(✅ ZAP scan is clean)*
- [ ] Are passwords securely hashed using a strong algorithm (e.g., bcrypt, Argon2)? *(⚠️ Backend check needed)*
- [ ] Are data backup and recovery processes GDPR-compliant? *(⚠️ Out of scope for scan)*
- [ ] Is personal data stored in data centers located within the EU? *(⚠️ Infrastructure not reviewed)*

## 🧩 Data Anonymization and Pseudonymization
- [ ] Is personal data anonymized where possible? *(⚠️ Not verified)*
- [ ] Are pseudonymization techniques used to protect data while maintaining utility? *(⚠️ Unknown)*

## 🧾 Data Subject Rights
- [ ] Can users download or request all personal data related to them (data access request)? *(⚠️ Feature not visible)*
- [ ] Is there an interface or process for users to request the deletion of their personal data? *(⚠️ Unknown)*
- [ ] Can users withdraw their consent for data processing? *(⚠️ Consent form missing)*

## 📄 Documentation and Communication
- [ ] Is there a privacy policy available to users during registration and easily accessible? *(❌ Not included)*
- [ ] Are administrators and developers provided with documented data protection practices? *(⚠️ Unknown)*
- [ ] Is there a documented data breach response process? *(❌ Not available)*

---

**Legend:**  
✅ = Implemented  
❌ = Missing  
⚠️ = Needs Manual Review  
[x] = Pass  
[ ] = To be checked

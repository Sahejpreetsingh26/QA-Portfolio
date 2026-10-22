# 🐛 Sample Defect Tracking Log & Lifecycle

This document records sample defects identified during execution of the E-Commerce functional test suite, tracking them from discovery through verification.

## 📊 Defect Log Matrix

| Bug ID | Module | Summary / Description | Severity | Priority | Status | Environment |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **BUG-001** | Authentication | Password reset link throws HTTP 500 internal server error on mobile web. | **Critical** | **P1** | **Open** | Mobile Safari (iOS 17) |
| **BUG-002** | Shopping Cart | Item quantity selector allows decrementing below 1, resulting in negative cart value. | **Major** | **P2** | **In Progress** | Chrome (Desktop) |
| **BUG-003** | Checkout | Applied discount code string is case-sensitive, rejecting valid lowercase input (e.g., "SAVE20"). | **Minor** | **P3** | **Closed / Verified** | Firefox (Desktop) |
| **BUG-004** | User Profile | User avatar image upload fails silently when file size exceeds 5MB limit. | **Major** | **P2** | **Ready for Retest** | Android Chrome |

---

## 🔄 Defect Lifecycle Stages Used:
* **New / Open:** Defect is newly logged and awaiting triage.
* **In Progress:** Developers are actively debugging and patching the code.
* **Ready for Retest:** Fix deployed to staging environment; pending QA verification.
* **Closed:** Fix verified successfully by QA.

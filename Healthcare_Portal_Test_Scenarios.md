# 🏥 Healthcare Portal QA Test Scenario Suite (Medica Insurance Portal)

This document outlines core functional, cross-platform, and responsive test scenarios designed for US healthcare member portals. It covers critical user journeys such as claims processing, digital ID card retrieval, plan benefits verification, and provider directory searches, ensuring HIPAA compliance and seamless user experience across Web, iOS, and Android platforms.

---

## 📋 Table of Contents
1. [User Authentication & Security (HIPAA Compliance)](#1-user-authentication--security-hipaa-compliance)
2. [Claims Processing & Status Workflows](#2-claims-processing--status-workflows)
3. [Digital ID Card Management](#3-digital-id-card-management)
4. [Provider Directory Search & Filters](#4-provider-directory-search--filters)
5. [Cross-Browser & Multi-Device Compatibility](#5-cross-browser--multi-device-compatibility)

---

### 1. User Authentication & Security (HIPAA Compliance)
* **TC_HC_001:** Verify that member login enforces multi-factor authentication (MFA) or secure OTP verification.
* **TC_HC_002:** Verify that session timeout occurs automatically after a period of inactivity (e.g., 15 minutes) to protect Protected Health Information (PHI).
* **TC_HC_003:** Verify that password reset links expire securely after a single use or within a strict time window (e.g., 30 minutes).
* **TC_HC_004:** Verify that failed login attempts trigger account lockout thresholds to prevent brute-force attacks.

---

### 2. Claims Processing & Status Workflows
* **TC_HC_005:** Verify that members can view a chronological list of recent medical, dental, and pharmacy claims.
* **TC_HC_006:** Verify claim status filtering options (e.g., *Processed, Pending, Denied*).
* **TC_HC_007:** Verify detailed claim breakdown views, including *Member Responsibility (Copay/Deductible)*, *Amount Billed*, and *Amount Paid by Plan*.
* **TC_HC_008:** Verify error handling when downloading Explanation of Benefits (EOB) PDF documents on low-bandwidth mobile networks.

---

### 3. Digital ID Card Management
* **TC_HC_009:** Verify that active member ID cards render correctly with accurate group numbers, member IDs, and copay tiers.
* **TC_HC_010:** Verify the "Download / Save as PDF" functionality for offline access on mobile devices.
* **TC_HC_011:** Verify that family members' dependent ID cards are accessible and switchable under the primary policyholder's profile.
* **TC_HC_012:** Verify that expired ID cards are automatically archived or updated when a new plan year begins.

---

### 4. Provider Directory Search & Filters
* **TC_HC_013:** Verify search functionality using zip code radius (e.g., within 5, 10, 25 miles) for in-network physicians and specialists.
* **TC_HC_014:** Verify advanced filtering options, including *Specialty, Accepting New Patients, Language Spoken, and Hospital Affiliation*.
* **TC_HC_015:** Verify that search results accurately display real-time network status (In-Network vs. Out-of-Network).
* **TC_HC_016:** Verify map integration pin accuracy and click-to-call phone number functionality on mobile responsive views.

---

### 5. Cross-Browser & Multi-Device Compatibility
* **TC_HC_017:** Verify layout stability and zero horizontal scrolling across desktop (Chrome, Safari, Firefox, Edge) and mobile emulators (iOS Safari, Android Chrome).
* **TC_HC_018:** Verify touch target spacing and font scaling for accessibility compliance on smaller mobile viewports.

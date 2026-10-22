# 🎓 ISTQB® Certified QA: Test Design Techniques & Risk Analysis

As an **ISTQB® Certified Software Quality Analyst (CTFL v4.0)**[cite: 7], I apply formal software testing principles, structured test design techniques, and risk-based quality strategies to minimize project risk and maximize test coverage.

---

## 📋 Table of Contents
1. [Core ISTQB Principles Applied in Practice](#1-core-istqb-principles-applied-in-practice)
2. [Black-Box Test Design Techniques](#2-black-box-test-design-techniques)
3. [Risk-Based Testing & Defect Management Strategy](#3-risk-based-testing--defect-management-strategy)

---

### 1. Core ISTQB Principles Applied in Practice
* **Testing shows presence, not absence of defects:** Testing reduces the probability of undiscovered defects remaining in the software, but it cannot prove the system is 100% defect-free.
* **Exhaustive testing is impossible:** Testing everything (all combinations of inputs and preconditions) is infeasible except for trivial cases. Application of *test design techniques* and *prioritization* is utilized to optimize test coverage.
* **Defect clustering:** A small number of modules or components typically contain the majority of discovered defects during pre-release testing. Focus testing effort on high-risk areas (e.g., checkout flows, payment gateways, auth modules).

---

### 2. Black-Box Test Design Techniques
Applied across e-commerce, healthcare portals, and SaaS platforms to derive systematic test cases:

* **Equivalence Partitioning (EP):** 
  * *Concept:* Dividing data input into valid and invalid partitions where all members of a partition are expected to behave similarly.
  * *Practical Example (e.g., Discount Percentage Input 1–100%):*
    * **Valid Partition:** `1 to 100` (Test data: `25`)
    * **Invalid Partition 1:** `< 1` (Test data: `0` or `-5`)
    * **Invalid Partition 2:** `> 100` (Test data: `101`)

* **Boundary Value Analysis (BVA):** 
  * *Concept:* Testing the boundary values of partitions, as errors are most frequently concentrated at the edges.
  * *Practical Example (e.g., Age Verification Minimum 18 Years):*
    * Test values checked: `17` (Invalid boundary-minus-one), `18` (Valid boundary minimum), `19` (Valid boundary-plus-one).

* **Decision Table Testing:**
  * *Concept:* Used for complex business logic with multiple logical conditions (e.g., User Role + Subscription Tier + Cart Value = Applied Discount Rule).

---

### 3. Risk-Based Testing & Defect Management Strategy
* **Product Risk Analysis:** Prioritizing testing resources based on *likelihood of failure* and *impact of failure*.
  * *High Risk / High Impact:* Payment processing gateway integration timeouts, HIPAA-compliant patient data leakage. (Tested first via extensive regression suites).
  * *Low Risk / Low Impact:* Minor footer styling alignment issues on desktop browsers. (Tested during final UI polish cycles).
* **Severity vs. Priority Classification:**
  * **Critical Severity / P1 Priority:** System crashes, data loss, absolute blockades of core user journeys. Requires immediate hotfix deployment.
  * **Minor Severity / P3 Priority:** Cosmetic text typos, layout shifts on obsolete viewports. Scheduled for minor release patches.

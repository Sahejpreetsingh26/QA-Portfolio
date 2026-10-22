# 🔄 Agile QA Lifecycle & Jira Defect Workflow

This document outlines my structured approach to Quality Assurance within Agile/Scrum sprint cycles. It defines the Software Testing Life Cycle (STLC) integration, Definition of Ready (DoR), Definition of Done (DoD), and defect triage management using tools like Jira, Asana, and WorkFront.

---

## 📋 Table of Contents
1. [STLC Integration in Agile Sprints](#1-stlc-integration-in-agile-sprints)
2. [Definition of Ready (DoR) & Definition of Done (DoD)](#2-definition-of-ready-dor--definition-of-done-dod)
3. [Jira Defect Lifecycle & State Transitions](#3-jira-defect-lifecycle--state-transitions)
4. [Bug Triage & Severity vs. Priority Matrix](#4-bug-triage--severity-vs-priority-matrix)

---

### 1. STLC Integration in Agile Sprints
As a QA Analyst, testing is integrated continuously across every phase of the Scrum sprint:
* **Sprint Planning:** Reviewing user stories, acceptance criteria, and technical designs early to identify ambiguities, testability gaps, and edge cases.
* **In-Sprint Testing:** Executing functional, sanity, and integration test cases concurrently as developers push features to staging environments.
* **Regression & Release Sign-Off:** Performing final end-to-end (E2E) regression suites, cross-browser checks, and verifying resolved Jira bug tickets prior to production deployment.

---

### 2. Definition of Ready (DoR) & Definition of Done (DoD)
* **Definition of Ready (DoR - When QA can start testing a story):**
  * User story includes clear, testable Acceptance Criteria (AC).
  * UI/UX designs/wireframes are attached (if applicable).
  * Backend API endpoints are documented or deployed to the test environment.
* **Definition of Done (DoD - When a feature is ready for release):**
  * All associated test cases executed and passed.
  * Zero Critical (P1) or High (P2) defects remaining unresolved.
  * Peer review and product owner sign-off completed.

---

### 3. Jira Defect Lifecycle & State Transitions
Standard workflow for tracking and resolving issues from discovery to verification:
1. **Open / To Do:** Defect is discovered, documented with reproduction steps, logs, and screenshots, then logged in Jira.
2. **In Progress / Assigned:** Developer picks up the ticket, investigates the root cause, and implements a code fix.
3. **Ready for Retest (Resolved):** Developer deploys the fix to staging/QA environment; ticket is assigned back to QA.
4. **Verified / Closed:** QA re-tests the scenario, confirms the bug is fixed without regressions, and closes the ticket.
5. **Reopened:** If the bug persists or fix is incomplete, QA reopens the ticket with updated notes.

---

### 4. Bug Triage & Severity vs. Priority Matrix
* **Severity (Technical Impact on System):**
  * **Critical:** System crash, data loss, security vulnerability, complete block of core revenue/checkout flow.
  * **Major:** Core feature broken with no workaround available.
  * **Minor:** Cosmetic issue, minor text typo, or non-blocking UI misalignment.
* **Priority (Business Urgency for Fix):**
  * **P1 (High):** Must be fixed immediately before any release (blocks testing or deployment).
  * **P2 (Medium):** Should be fixed in the current sprint.
  * **P3 (Low):** Can be deferred to a future backlog grooming session.

# Corporate Actions Event Notification & Exception Tracker

## 📌 Executive Summary
This repository details the business analysis, Agile user backlog, and technical requirements for an automated Corporate Actions Processing Engine. The system manages Mandatory and Voluntary corporate events (Dividends, Stock Splits, Rights Issues) across global custody accounts, focusing on parsing SWIFT MT564 messages and mitigating operational risk.

---

## 🎯 Business Problem & Solution
Processing voluntary corporate actions requires strict adherence to market election deadlines. Missed elections or data entry errors can result in significant financial loss. This platform automates SWIFT notification ingestion, tracks client election responses, and flags exceptions before market cutoff times.

---

## 📂 Repository Structure
```
corporate-actions-exception-tracker/
├── docs/
│   ├── User_Stories_Jira_Backlog.md
│   ├── Data_Dictionary_SWIFT_MT564.md
│   └── Exception_Handling_Workflow.md
└── README.md
```

---

## 📝 Featured User Stories & Acceptance Criteria

### Story 1: SWIFT MT564 Parsing & Notification Ingestion
* **As a** Custody Operations Analyst,
* **I want** the system to parse incoming SWIFT MT564 messages automatically,
* **So that** corporate action event details (ISIN, Ex-Date, Record Date, Pay Date) are logged without manual intervention.

**Acceptance Criteria (Gherkin Format):**
* **Given** a valid MT564 message is received from a clearing depository,
* **When** the ingestion engine processes the payload,
* **Then** all core event dates and parameters must populate in the database within 5 seconds with >99.9% accuracy.

---

### Story 2: Client Election Deadline Notification Alert
* **As a** Relationship / Business Development Analyst,
* **I want** automated notifications sent to clients 48 hours prior to voluntary election cutoffs,
* **So that** client instructions are received prior to market deadlines.

---

## 📑 Agile Backlog Summary

| Epic | Story ID | Summary | Points | Priority |
| :--- | :--- | :--- | :--- | :--- |
| **Ingestion** | CA-101 | Parse incoming SWIFT MT564 notifications into internal DB | 8 | High (P1) |
| **Elections** | CA-102 | Build election submission portal for Voluntary Events | 5 | High (P1) |
| **Exceptions**| CA-103 | Implement Break Resolution Workflow for entitlement errors | 5 | Medium (P2) |
| **Reporting** | CA-104 | Export daily client position entitlement reports (Excel/CSV) | 3 | Low (P3) |

---

## 🛠️ Domain & Technical Skills
* **Custody Operations:** Corporate Actions (Mandatory/Voluntary), SWIFT Standards (MT564, MT568), Securities Services.
* **Agile BA:** Backlog Refinement, User Story Writing, Acceptance Criteria Definition, Jira & Confluence.

---
*Created by [Paulina Ukata](https://www.linkedin.com/in/paulina-ukata-6281902b4/) for Business Analyst Portfolio.*

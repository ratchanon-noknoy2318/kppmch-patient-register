# KPPMCH Patient Registration

| PROJECT HEADER |
| :--- |
| **LINE Group & Google Apps Script Integration** |
| [![Project Header](https://kppmch-register.vercel.app/og-image.png)](https://kppmch-register.vercel.app/) |

---

| PROJECT GENESIS & REQUIREMENTS |
| :--- |
| **Source of Requirements** |
| This system was developed based on specific requirements from **Senior Professional Level Nurses (พยาบาลวิชาชีพชำนาญการพิเศษ)** to solve ward-level registration bottlenecks and ensure clinical data integrity. |

---

| ACTIVITY & REPORTING | | |
| :--- | :--- | :--- |
| **Category** | **Detail** | **Link / Reference** |
| Official Recognition | Public Health Innovation | [kppmu.go.th/news-detail](https://www.kppmu.go.th/news-detail?hd=1&id=124000) |
| Live Dashboard | **Looker Studio (Real-time)** | [View Executive Dashboard](https://lookerstudio.google.com/u/0/reporting/9a9e9348-d32c-4577-ba31-33bcea283fee/page/page_12345) |
| Project Status | Official Implementation | Registered Municipal Innovation |

---

| CLINICAL QUALITY & NURSING MANAGEMENT | | |
| :--- | :--- | :--- |
| **Focus Area** | **Nursing Standard** | **Strategic Outcome** |
| Patient Safety | Right Person, Right Record | 100% Accuracy in National ID Verification |
| Workflow Optimization | Lean Nursing Process | Reduced Administrative Time for Ward Nurses |
| Data-Driven Decisions | Real-time Bed/Case Monitoring | Enhanced Resource Allocation for Special Care |
| Quality Assurance | Continuous Quality Improvement (CQI) | Systematic Data Audit for Accreditation (HA/JCI) |

---

| 1. SYSTEM ARCHITECTURE MATRIX | | |
| :--- | :--- | :--- |
| **Layer** | **Component** | **Functional Role** |
| Frontend | KPPMCH Web App | User Interface & Registration Entry |
| Interface | LINE Messaging API | Event-Driven Webhook Gateway |
| Logic | Google Apps Script | Serverless Transaction Processing |
| Database | Google Sheets | Structured Clinical Data Storage |
| Reporting | **Looker Studio** | **Executive Data Visualization** |

---

| 2. AUTOMATION & TECHNICAL WORKFLOW | | |
| :--- | :--- | :--- |
| **Process** | **Method** | **Operational Outcome** |
| Tracking | `source.groupId` | Automated Ward-level Segregation |
| Capture | Regex `(\d{13})` | Zero-Error National ID Extraction |
| Validation | Conditional Logic | Duplicate Entry & Format Protection |
| Analytics | Data Connector | Automated Sync to Looker Studio |

---

| 3. DATA GOVERNANCE (PDPA & ETHICS) | | |
| :--- | :--- | :--- |
| **Attribute** | **Extraction Source** | **Compliance Detail** |
| Department | `event.source.groupId` | Purpose-based Isolation (Ward-specific) |
| Timestamp | `event.timestamp` | Audit Trail for Nursing Documentation |
| Citizen ID | Regex Match | Restricted Access to Sensitive Data |
| Compliance | PDPA Standards | Secure Storage of Patient Identifiers |

---

| 4. IMPLEMENTATION FRAMEWORK | | |
| :--- | :--- | :--- |
| **Step** | **Phase** | **Task** |
| **0** | **Requirement** | **Clinical Need Assessment with Senior Nursing Staff** |
| 1 | Database | Initialize Sheets with Master Headers |
| 2 | Backend | Deploy GAS API Endpoint |
| 3 | Integration | Bind Webhook to LINE Developer Console |
| 4 | **Reporting** | **Connect Dataset to Looker Studio Dashboard** |

---

| 5. CONTACT & CREDITS | |
| :--- | :--- |
| **Author** | Ratchanon Noknoy |
| **LinkedIn** | [linkedin.com/in/ratchanon-noknoy/](https://www.linkedin.com/in/ratchanon-noknoy/) |
| **GitHub** | [github.com/Ratchanon2318](https://github.com/Ratchanon2318) |
| **License** | MIT © 2026 |

# KPPMCH Telemedicine Registration
**LINE Group & Google Apps Script Integration**

[![Project Header](https://kppmch-register.vercel.app/og-image.png)](https://kppmch-register.vercel.app/)

---

## Activity Recognition
[![Kamphaeng Phet Municipality](https://img.shields.io/badge/Activity-Public%20Health%20Innovation-blue?style=for-the-badge&logo=google-cloud&logoColor=white)](https://www.kppmu.go.th/news-detail?hd=1&id=124000)
**Organization:** Kamphaeng Phet Municipality Community Hospital (KPPMCH)  
**Reference:** [Public Health Service Innovation - kppmu.go.th](https://www.kppmu.go.th/news-detail?hd=1&id=124000)

---

## 1. System Architecture
| Layer | Component | Specification |
| :--- | :--- | :--- |
| **Frontend** | KPPMCH Web App | kppmch-register.vercel.app |
| **Interface** | LINE Messaging API | Group Webhook Context |
| **Logic** | Google Apps Script | Serverless API Handler |
| **Database** | Google Sheets | Structured Clinical Logs |

---

## 2. Technical Workflow
| Process | Method | Action |
| :--- | :--- | :--- |
| **Tracking** | `source.groupId` | Segregate data by Clinical Ward |
| **Capture** | Regex: `(\d{13})` | Auto-extract National ID |
| **Validation** | Conditional Logic | Check format and duplicate entries |
| **Sync** | `UrlFetchApp` | Real-time feedback to LINE Group |

---

## 3. Data Mapping & PDPA Compliance
| Field | Data Source | Compliance Detail |
| :--- | :--- | :--- |
| **Department** | `event.source.groupId` | Ward-level data isolation |
| **Timestamp** | `event.timestamp` | Transaction logging |
| **Patient Name** | Text Parsing | Purpose-based collection only |
| **Citizen ID** | Regex Match | Protected Sheet access |

---

## 4. Implementation Framework
| Step | Category | Task |
| :--- | :--- | :--- |
| **1** | Database | Prepare Sheets with KPPMCH Headers |
| **2** | Backend | Deploy GAS Web App (Access: Anyone) |
| **3** | API Link | Bind GAS URL to LINE Webhook |
| **4** | Testing | Verify data flow from Group to Sheets |

---

## 5. Developer & Contact
| Type | Detail |
| :--- | :--- |
| **Author** | Ratchanon Noknoy |
| **License** | MIT © 2026 |
| **LinkedIn** | [linkedin.com/in/ratchanon-noknoy/](https://www.linkedin.com/in/ratchanon-noknoy/) |
| **GitHub** | [github.com/Ratchanon2318](https://github.com/Ratchanon2318) |

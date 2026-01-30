# KPPMCH Telemedicine Registration
**LINE Group & Google Apps Script Integration**

[![Project Header](https://kppmch-register.vercel.app/og-image.png)](https://kppmch-register.vercel.app/)

---

## Activity & Reporting
| Category | Detail | Link / Reference |
| :--- | :--- | :--- |
| **Official Recognition** | Public Health Innovation | [kppmu.go.th/news-detail](https://www.kppmu.go.th/news-detail?hd=1&id=124000) |
| **Live Dashboard** | **Looker Studio (Real-time)** | [View Executive Dashboard](https://lookerstudio.google.com/u/0/reporting/9a9e9348-d32c-4577-ba31-33bcea283fee/page/page_12345) |
| **Project Status** | Official Implementation | Registered Municipal Innovation |

---

## 1. System Architecture Matrix
| Layer | Component | Functional Role |
| :--- | :--- | :--- |
| **Frontend** | KPPMCH Web App | User Interface & Registration Entry |
| **Interface** | LINE Messaging API | Event-Driven Webhook Gateway |
| **Logic** | Google Apps Script | Serverless Transaction Processing |
| **Database** | Google Sheets | Structured Clinical Data Storage |
| **Reporting** | **Looker Studio** | **Executive Data Visualization** |

---

## 2. Automation & Technical Workflow
| Process | Method | Operational Outcome |
| :--- | :--- | :--- |
| **Tracking** | `source.groupId` | Automated Ward-level Segregation |
| **Capture** | Regex `(\d{13})` | Zero-Error National ID Extraction |
| **Validation** | Conditional Logic | Duplicate Entry & Format Protection |
| **Analytics** | Data Connector | Automated Sync to Looker Studio |

---

## 3. Data Governance (PDPA Structure)
| Attribute | Extraction Source | Compliance Detail |
| :--- | :--- | :--- |
| **Department** | `event.source.groupId` | Purpose-based Isolation |
| **Timestamp** | `event.timestamp` | Audit Trail Integrity |
| **Citizen ID** | Regex Match | Restricted Data Access Controls |

---

## 4. Implementation Framework
| Step | Phase | Task |
| :--- | :--- | :--- |
| **1** | Database | Initialize Sheets with Master Headers |
| **2** | Backend | Deploy GAS API Endpoint |
| **3** | Integration | Bind Webhook to LINE Developer Console |
| **4** | **Reporting** | **Connect Dataset to Looker Studio Dashboard** |

---

## 5. Contact & Credits
| Type | Detail |
| :--- | :--- |
| **Author** | Ratchanon Noknoy |
| **LinkedIn** | [linkedin.com/in/ratchanon-noknoy/](https://www.linkedin.com/in/ratchanon-noknoy/) |
| **GitHub** | [github.com/Ratchanon2318](https://github.com/Ratchanon2318) |
| **License** | MIT © 2026 |

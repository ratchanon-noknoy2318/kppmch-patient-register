# KPPMCH Telemedicine Registration
**LINE Group & Google Apps Script Integration**

---

![Project Header](https://kppmch-register.vercel.app/og-image.png)

---

## 1. System Architecture
| Layer | Component | Specification |
| :--- | :--- | :--- |
| Frontend | KPPMCH Web App | kppmch-register.vercel.app |
| Interface | LINE Messaging API | Group Webhook Context |
| Logic | Google Apps Script | Serverless API Handler |
| Database | Google Sheets | Structured Clinical Logs |

---

## 2. Technical Workflow
| Process | Method | Action |
| :--- | :--- | :--- |
| Tracking | source.groupId | Segregate data by Clinical Ward |
| Capture | Regex: (\d{13}) | Auto-extract National ID |
| Validation | Conditional Logic | Check format and duplicate entries |
| Sync | UrlFetchApp | Real-time feedback to LINE Group |

---

## 3. Data Mapping & PDPA
| Field | Data Source | Compliance Detail |
| :--- | :--- | :--- |
| Department | event.source.groupId | Ward-level data isolation |
| Timestamp | event.timestamp | Transaction logging |
| Patient Name | Text Parsing | Purpose-based collection only |
| Citizen ID | Regex Match | Encrypted/Protected Sheet access |

---

## 4. Implementation Steps
| Step | Category | Task |
| :--- | :--- | :--- |
| 1 | Database | Prepare Sheets with KPPMCH Headers |
| 2 | Backend | Deploy GAS Web App (Access: Anyone) |
| 3 | API Link | Bind GAS URL to LINE Webhook |
| 4 | Testing | Verify data flow from Group to Sheets |

---

## 5. Contact & License
| Type | Detail |
| :--- | :--- |
| Author | Ratchanon Noknoy |
| License | MIT © 2026 |
| LinkedIn | https://www.linkedin.com/in/ratchanon-noknoy/ |
| GitHub | https://github.com/Ratchanon2318 |

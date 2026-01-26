# KPPMCH Telemedicine Registration
**LINE Group & Google Apps Script Integration**

---

## 1. System Architecture



| Layer | Component | Specification |
| :--- | :--- | :--- |
| **Frontend** | KPPMCH Web App | [kppmch-register.vercel.app](https://kppmch-register.vercel.app/) |
| **Interface** | LINE Messaging API | Group Webhook Context |
| **Logic** | Google Apps Script | Serverless API Handler |
| **Database** | Google Sheets | Structured Clinical Logs |

---

## 2. Technical Workflow

| Process | Method | Action |
| :--- | :--- | :--- |
| **Tracking** | source.groupId | Segregate data by Clinical Ward |
| **Capture** | Regex: `(\d{13})` | Auto-extract National ID |
| **Validation** | Conditional Logic | Check format & duplicate entries |
| **Sync** | UrlFetchApp | Real-time feedback to LINE Group |

---

## 3. Data Mapping Schema

| Field | Data Source | Target Column |
| :--- | :--- | :--- |
| **Department** | event.source.groupId | Column A (Source) |
| **Timestamp** | event.timestamp | Column B (Date/Time) |
| **Patient Name** | Text Parsing | Column C (Name) |
| **Citizen ID** | Regex Match | Column D (ID Number) |

---

## 4. Implementation Steps

| Step | Category | Task |
| :--- | :--- | :--- |
| **1** | **Database** | Prepare Sheets with KPPMCH Headers |
| **2** | **Backend** | Deploy GAS Web App (Access: Anyone) |
| **3** | **API Link** | Bind GAS URL to LINE Webhook |
| **4** | **Testing** | Verify data flow from Group to Sheets |

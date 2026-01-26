# Telemedicine Registration System
**Group-based Patient Monitoring via LINE Messaging API & Google Apps Script**

---

## 1. Core System Infrastructure

| Layer | Component | Technical Specification |
| :--- | :--- | :--- |
| **Backend** | Google Apps Script | Serverless V8 Engine / Webhook Endpoint |
| **Interface** | LINE Messaging API | Group Messaging Context / Event Handlers |
| **Database** | Google Sheets | Structured Data Storage / Multi-tab Support |
| **Security** | SHA256 HMAC | X-Line-Signature Payload Verification |

---

## 2. Group-Centric Operational Logic

| Operational Aspect | Implementation Logic | System Outcome |
| :--- | :--- | :--- |
| **Identity Management** | source.groupId Extraction | Segregates data by hospital department |
| **Broadcast Scope** | replyToken / pushMessage | Multicast notifications to all group staff |
| **Command Control** | Switch-case String Parsing | Trigger admin functions via group chat |
| **Data Separation** | Group-to-Sheet Mapping | Unique sheets assigned per Group ID |

---

## 3. Data Governance & Automation

| Function | Logic Implementation | Automation Value |
| :--- | :--- | :--- |
| **Data Extraction** | Regex: `/(\d{13})/g` | Automatic parsing of National ID numbers |
| **Validation** | Conditional Logic (if/else) | Prevents null or incorrectly formatted entries |
| **Maintenance** | Time-driven Triggers | Daily auto-archive of processed records |
| **Sync Protocol** | UrlFetchApp (POST) | Real-time status confirmation to LINE Group |

---

## 4. Implementation Roadmap

| Phase | Task | Key Action |
| :--- | :--- | :--- |
| **Setup** | Environment Prep | Define Sheet Columns: ID, Time, Name, Status |
| **Coding** | GAS Development | Deploy doPost(e) with Messaging API logic |
| **Security** | Auth Configuration | Set Channel Access Token as Script Property |
| **Linkage** | Webhook Integration | Register GAS Web App URL in LINE Console |
| **Deployment** | UAT & Verification | Validate data flow from LINE Group to Sheets |

---

## 5. Message Parsing Schema (Standard)

| Input Field | Parsing Pattern | Target Sheet Column |
| :--- | :--- | :--- |
| **Patient Name** | String split / Regex | Column C (Name) |
| **ID Number** | 13-digit numeric check | Column D (National ID) |
| **Timestamp** | event.timestamp (Epoch) | Column B (Registration Time) |
| **Source ID** | event.source.groupId | Column A (Department ID) |

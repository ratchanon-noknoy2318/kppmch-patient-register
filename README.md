# KPPMCH Patient Registration

| PROJECT ARCHITECTURE OVERVIEW |
| :--- |
| **High-Level System Design & Clinical Integration** |
| [![Project Header](https://kppmch-register.vercel.app/og-image.png)](https://kppmch-register.vercel.app/) |

---

| 1. CORE SYSTEM ARCHITECTURE | | |
| :--- | :--- | :--- |
| **Component** | **Technology Stack** | **Architectural Responsibility** |
| **Client Interface** | LIFF / Web Application | Provides a sanitized UI for data entry, bypassing chat limitations. |
| **Messaging Gateway** | LINE Messaging API | Acts as an Event-Driven Webhook to capture group-specific metadata. |
| **Serverless Logic** | Google Apps Script (GAS) | Execution of business logic, Regex parsing, and API routing. |
| **Cloud Storage** | Google Sheets API | Serves as a lightweight NoSQL-style database for rapid deployment. |
| **BI Layer** | Looker Studio Connector | Direct abstraction of raw data into executive-level KPIs. |

---

| 2. TECHNICAL DATA FLOW | | |
| :--- | :--- | :--- |
| **Sequence** | **Action** | **Technical Detail** |
| **Input** | User Registration | Data submitted via Webhook with `groupId` and `userId` context. |
| **Processing** | Regex Extraction | Validation of 13-digit ID via `RegExp` pattern matching in GAS. |
| **Storage** | Append Row | Atomic write operation to specific Sheet tabs based on Ward ID. |
| **Security** | Payload Verification | Ensures requests originate from authorized LINE Webhook signatures. |

---

| 3. NURSING MANAGEMENT ARCHITECTURE | | |
| :--- | :--- | :--- |
| **Requirement Source** | **Senior Professional Nurse** | **Requirement Fulfillment** |
| **Ward Isolation** | Multi-tenant Design | Data is automatically segregated by LINE `groupId` (One group per Ward). |
| **Audit Ability** | Traceability Schema | Every entry is logged with a Server-Side Timestamp and User Metadata. |
| **Performance** | Low-Latency Entry | Optimized for fast-paced clinical environments (Zero login required). |

---

| 4. DATA GOVERNANCE & PDPA ARCHITECTURE | | |
| :--- | :--- | :--- |
| **Layer** | **Method** | **Security Detail** |
| **Encryption** | HTTPS / TLS 1.3 | All data in transit between LINE and GAS is fully encrypted. |
| **Access Control** | Spreadsheet Sharing | Data access is restricted via Google Workspace IAM roles. |
| **Privacy** | Minimal Data Capture | Only necessary Patient Identifiers are extracted via Regex. |

---

| 5. DEPLOYMENT & SCALABILITY | | |
| :--- | :--- | :--- |
| **Phase** | **Action Item** | **Strategic Goal** |
| **Requirement** | **Clinical Needs Analysis** | **Aligned with Senior Professional Nursing Standards.** |
| **Development** | GAS Web App Deployment | Implementation of `doPost(e)` handlers for real-time processing. |
| **Integration** | Webhook Tunneling | Establishing the link between LINE Developers Console and Cloud script. |
| **Monitoring** | Dashboard Binding | Mapping Sheet headers to Looker Studio dimensions and metrics. |

---

| 6. CONTACT & CREDITS | |
| :--- | :--- |
| **Architect** | Ratchanon Noknoy |
| **LinkedIn** | [linkedin.com/in/ratchanon-noknoy/](https://www.linkedin.com/in/ratchanon-noknoy/) |
| **GitHub** | [github.com/Ratchanon2318](https://github.com/Ratchanon2318) |
| **License** | MIT © 2026 |

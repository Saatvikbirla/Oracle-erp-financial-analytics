# Enterprise Oracle Cloud ERP Financial Analytics Portfolio
**Domain:** Financials & Supply Chain Management (FSCM) — Accounts Payable Ledger  
**Developer:** Saatvik Birla  

---

## 🏛️ Repository Overview
This repository contains a comprehensive suite of end-to-end data analytics and business intelligence assets engineered directly inside the Oracle Fusion Cloud ERP ecosystem. It demonstrates proficiency in navigating complex corporate data structures, creating performant logical semantics, writing backend database scripts, and building pixel-perfect financial report deliverables.

---

## 📊 Project 1: Real-Time Accounts Payable Executive Dashboard
**Category:** Strategic Business Intelligence & Operational Monitoring  
**Core Tool:** Oracle Transactional Business Intelligence (OTBI)  
**Data Layer:** `Payables - Invoices Transactions Real Time` Subject Area

### 📌 Business Problem & Core Objectives
Corporate finance executives suffer from informational lag when dealing with high-volume transactional ledgers. Standard transactional rows obscure crucial macro insights like working capital tied up in approval bottlenecks, supplier risk concentrations, and cash flow trends. 

This project solves this by constructing a unified executive command deck built on top of real-time transactional streams.

### 🛠️ Key Architectural Components
* **High-Impact KPI Radar:** Engineered real-time summary containers utilizing custom application formatting filters to isolate core operational health metrics including *Total Unpaid Invoices Amount*, *Total Approved Amount*, and *Pending Validation Volume*.
* **Dynamic Time-Series Analytics:** Modeled a multi-dimensional spend trend line chart mapping historic payment behavior, giving managers clear visibility into quarterly cash outflow cycles.
* **Supplier Concentration Risk Grid:** Constructed a multi-attribute data table utilizing complex conditional metadata logic to automatically highlight exposure levels exceeding critical enterprise safety thresholds in red.
* **Interactive Semantic Filtering:** Built a global prompt controller dashboard interface. When a user filters by a specific Business Unit or Vendor, the criteria are passed downward, causing all dashboard components to recalculate concurrently.

### 📁 Source Directory
* `/AP_Exec_Dashboard/` -> Contains the binary `.catalog` system transport file along with the individual underlying structural XML configurations.

---

## 🖨️ Project 2: Pixel-Perfect Global Operational Invoice Package
**Category:** Compliance Document Engineering & Operational Reporting  
**Core Tool:** BI Publisher (BIP)  
**Data Layer:** Direct SQL Relational Modeling via `ApplicationDB_FSCM`

### 📌 Business Problem & Core Objectives
While drag-and-drop subject areas work well for high-level dashboards, corporate compliance requires highly structured, tamper-proof document attachments (like invoice registers or check printouts) that pull data straight from the database and must comply with exact, branded typography rules.

This project bypasses user application abstractions to query backend database ledger tables directly and generate printable audit documents.

### 🛠️ Key Architectural Components
* **Direct Relational Database Modeling (`AP_Invoice_Package_DM`):** Written an optimized direct SQL join statement pulling straight from production tables (`ap_invoices_all` and `poz_suppliers_v`). 
* **Legacy Join Protocols:** Utilized classic Oracle `(+)` outer join notation within the relational mapping layers to guarantee complete data retention, ensuring the document renders historical invoice lines smoothly even if corresponding master supplier parameter properties are null.
* **Manual XSL-FO Template Engineering:** Hand-coded a complete, lightweight Rich Text Format (`.rtf`) layout layout from scratch. Embedded advanced control block markers (`<?for-each:G_1?>` ... `<?end for-each?>`) to direct the core XML publisher compilation engine to clone tabular frameworks dynamically at runtime.
* **Typographical Field Modifiers:** Written custom data-handling masks directly inside data cell nodes to convert raw database timestamps and convert unformatted floats into clean accounting currency text strings (`<?format-number:FIELD; '999,G99,D00'?>`).

### 📁 Source Directory
* `/AP_Invoice_Report/` -> Contains the raw schema database layout (`.xml`) blueprint alongside the manual hand-coded stylesheet template layout (`.rtf`).

---

## 🚀 Technical Skills Verified Across This Portfolio
* **ERP Domain Expertise:** In-depth understanding of Oracle Fusion Financials ledger structures, supplier tables, and business unit org tracking.
* **Data Pipelines & Engineering:** Direct SQL query design, database optimization, schema parsing, and hierarchical XML processing.
* **UI/UX Document Design:** Advanced visual data alignment, custom color grouping, interactive dashboard composition, and responsive analytical design.

# Real-Time Accounts Payable Executive Dashboard
**Domain:** Oracle Cloud ERP (Financials)  
**Technologies:** Oracle Transactional Business Intelligence (OTBI), Oracle Fusion Applications, Analytics Semantic Layer, XML Analytics Metadata

## 📌 Project Overview
Designed and deployed an enterprise-grade financial intelligence dashboard within Oracle Fusion Cloud ERP. This cockpit provides corporate executives with an instantaneous radar of accounts payable metrics, workflow processing statuses, and liability exposure trajectories.

Rather than generating flat operational data listings, this solution implements dynamic multi-parameter state filtering and visual anomaly alerts to drastically reduce an executive's time-to-insight.

## 🛠️ Key Technical Architecture & Implementation
The project is built modularly using separate analysis definitions joined on a shared dashboard canvas layout:

1. **Global Dynamic Control Filter (`AP_Executive_Dashboard_Prompt`)**
   * Implements multi-select choice lists bound to `"Supplier"."Supplier Name"` and `"Invoice Details"."Approval Status"`.
   * Integrates a continuous calendar date range picker utilizing the `is between` SQL comparison operator.
   * Leverages `is prompted` event listeners to broadcast state selections downstream across all page components simultaneously.

2. **Executive Strategic KPI Summary Cards (`AP_Executive_KPI_Tiles`)**
   * Aggregates real-time financial metrics: Total Invoice Liability (`SUM`), Total Cash Outflow (`SUM`), and Active Document Processing Volume via an optimized `COUNT(DISTINCT "Invoice Number")` expression.

3. **Time-Series Spend Trajectory Graph (`AP_Executive_Spend_Trend`)**
   * Formats raw transactional ledger timestamps chronologically into aggregated year-month periods.
   * Maps aggregate spend volume onto an interactive time-series line plot to display historical corporate liability trends.

4. **Supplier Operational Bottleneck Pivot Matrix (`AP_Supplier_Vulnerability_Matrix`)**
   * Transforms flat transaction arrays into a multi-dimensional cross-tab spreadsheet layout.
   * Columns scale dynamically across `Approval Status` attributes to segment processing pipelines.
   * **Conditional Optimization:** Implements inline metadata rules targeting records where exposure exceeds a specific fiscal threshold, altering cells to a high-visibility text layout for rapid risk identification.

## 📁 Repository Structure
* `/Financial_Analytics_Portfolio.catalog` -> Complete binary archive file for direct import/migration deployment into any standard Oracle BI instance.
* `/source-xml/` -> Extracted logical metadata code configurations for individual analyses.
* `/documentation/` -> Screenshots showing full multi-filter dashboard interactions and visual alerts.

## 🚀 Impact & Insights
* **Consolidated Overhead:** Replaced the necessity for 50+ individual vendor reports with a single, highly interactive analytical cockpit.
* **Operational Auditing:** Enabled AP managers to isolate workflow bottlenecks (e.g., invoices stuck in 'Pending Approval') within 2 clicks.

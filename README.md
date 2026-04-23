# RPT2000 — Comparative Financial Analytics & Data Transformation

The **RPT2000** program is an enhanced COBOL reporting utility designed for comparative financial analysis. Building upon its predecessor, this version processes customer financial records from a master input file (`CUSTMAST`) to generate a formatted, multi-columnar Year-To-Date (YTD) Sales Report that highlights performance variances.

## What it does
* **Comparative Analytics:** Automatically calculates the **Change Amount** (Current YTD - Last YTD) and the **Change Percent** for every customer record.
* **Grand Totals & Aggregation:** Accurately summarizes all individual metrics to provide a final company-wide performance overview.
* **Dynamic Page Management:** Features an automated page-breaking system with standardized headers, real-time date/time stamps, and clean visual separators.
* **Advanced Data Editing:** Utilizes numeric-edited picture clauses (e.g., `ZZ,ZZ9.99-`) to ensure professional accounting-style output, specifically for negative variance values.
* **Data Transformation:** Seamlessly converts raw record data—including branch numbers, sales rep IDs, and customer names—into a structured audit trail.

## New COBOL Concepts Implemented
Compared to the foundational **RPT1000**, this version introduces more complex arithmetic and logic:
* **Arithmetic Variance Logic:** Implementation of `SUBTRACT` and `COMPUTE` statements specifically for financial variance analysis.
* **Zero-Division Guarding:** Proactive logic-based checks to prevent system crashes when calculating percentages for accounts with no prior sales history.
* **JCL Step Synchronization:** Precise integration between internal COBOL `FILE-CONTROL` and external Job Control Language (JCL) `DD` names for mainframe execution.
* **COBOL ALL Clauses:** Strategic use of the `ALL` figurative constant to generate standardized visual dividers across large-scale reports.

## Program Output

Below is the execution result of the RPT2000 program, showcasing the comparative metrics and formatted sales headers:

![Program Output](asset/CodeOutput2.png)

---

### Author Profiles
* [Clay Rasmussen - GitHub](https://github.com/Clay-Rasmussen)
* [Tristan Joubert - GitHub](https://github.com/TJoubert004)

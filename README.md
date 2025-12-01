# ab-testing-e-commerce
# 📈 E-commerce Feature Validation through A/B Testing: Button Redesign

## Project Goal
The core objective of this project was to provide a rigorous statistical evaluation of an A/B test focused on implementing a **larger checkout button on the main page**. The primary goal was to increase the `begin_checkout` rate by 5% without negatively impacting `session with orders`.

## Key Business Results
- **Overall Conclusion:** The test **failed to show a significant difference** for the overall audience (`p = 0.27`).
- **Deep Segment Analysis:** Significant negative impacts were discovered within key segments, highlighting the need for detailed analysis:
    * **Tablet Users:** Variant B (new design) was **significantly less successful** (`p < 0.001`) with tablet users, showing a sharp drop in `begin_checkout`.
    * **Europe Segment:** A statistically significant deterioration in `begin_checkout` was observed in the European market.
- **Recommendation:** Recommended to **reject full deployment** of Variant B and prioritize technical analysis and design optimization for the Tablet segment.

## Technology Stack & Methodology
* **Data Retrieval & Metric Calculation:** **SQL** (for querying data, defining control/experiment groups, and calculating core metrics).
* **Statistical Analysis:** **Google Sheets** or similar tools were used for calculating P-values, Z-score, and confidence intervals based on extracted data.
* **Visualization & Segment Analysis:** **Tableau / Power BI** (for visualizing user distribution across groups/segments and identifying localized performance issues).
* **Deliverables:** SQL Query file, Tableau/BI Dashboard link (or screenshot), and A/B Test Card (Summary).

## Project Workflow
1.  **Data Extraction (SQL):** Wrote and executed complex SQL queries to pull raw session and event data for Control and Experimental groups.
2.  **Metric Calculation:** Defined and calculated the primary (`begin_checkout / session`) and guardrail (`session with orders / session`) metrics.
3.  **Statistical Testing:** Calculated statistical significance for the overall audience and key segments (Device, Continent, Channel).
4.  **Segmented Analysis:** Utilized BI tools to drill down into localized issues, confirming significant performance drops in the Tablet and European segments.
5.  **Conclusion & Next Steps:** Delivered a clear, data-backed recommendation to halt deployment and provided a strategy for future optimization.

## Access Code
The full SQL query used for data extraction and metric calculation is available in the file: **[Insert SQL Filename, e.g., `AB_Test_Query.sql`]**
The dashboard visualization link or screenshots are available here: **[Insert Dashboard Link/Screenshot file]**

# ab-testing-e-commerce
# E-commerce Feature Validation through A/B Testing: Button Redesign

## Project Goal
The core objective of this project was to provide a rigorous statistical evaluation of an A/B test focused on implementing a larger checkout button on the main page.
The primary goal was to increase the `begin_checkout` rate by 5% without negatively impacting `session with orders`.

## Key Business Results
- **Overall Conclusion:** The test failed to show a significant difference for the overall audience (`p = 0.27`), meaning the primary goal of increasing `begin_checkout` was not met.
The `session with orders` metric remained stable.
- **Deep Segment Analysis:** Although the overall result was neutral, significant negative impacts were discovered within key segments:
    * **Tablet Users:** Variant B (new design) was significantly less successful (`p < 0.001`) with tablet users, showing a sharp drop in `begin_checkout` (-25.68% for the event).
    * **Europe Segment:** A statistically significant deterioration in `begin_checkout` was observed in the European market.
    * **Organic Search Channel:** Showed a significant deterioration in `begin_checkout`.
- **Recommendation:** The recommendation was to **reject full deployment** of Variant B in its current form. Further steps include technical analysis and re-testing with device-specific and regional optimizations.

## Technology Stack & Methodology
* **Data Retrieval & Processing:** SQL (for initial data query and filtering), Python (Pandas, NumPy)
* **Statistical Analysis:** Used statistical testing (e.g., Z-test) for calculating P-values and confidence intervals at a **95% Confidence Level**.
* **Visualization:** Tableau (for visualizing user distribution across groups/segments).
* **Methodology:** Hypothesis testing, Sample validation (distribution was confirmed to be 50%/50% and correct).

## Project Workflow
1.  **Metric Definition:** Defined `begin_checkout / session` as the primary metric and `session with orders / session` as the guardrail metric.
2.  **Sample Validation:** Confirmed correct 50%/50% user distribution between Group 1 (Control) and Group 2 (Experimental).
3.  **Statistical Testing (Overall):** Performed analysis confirming **No significant difference** overall (`p=0.27`).
4.  **Segmented Analysis:** Conducted deep-dive analysis by **Device, Continent, and Channel** to detect localized performance issues.
5.  **Conclusion & Next Steps:** Provided clear, data-backed recommendations to halt deployment and investigate specific technical and design issues for the Tablet, European, and Organic Search segments.


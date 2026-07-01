# Brand versus Generic Product Competitive Analysis

**Business Question**: Is the average generic product financially competitive with the average branded product within the same category?

**Executive Summary**

Yes, on a like-for-like category basis, the average generic product is financially competitive with the average branded product, but the two win in different ways. Generics sell at a lower per-unit price than their branded counterparts (roughly 6% lower in OTC, 13% lower in Prescription), which caps their average revenue and margin per SKU. However, generics convert a higher share of that lower revenue into margin: the overall margin percentage for generic products is 25.7%, versus 24.5% for branded products.

The practical read: generics are not underperforming the portfolio, they are pricing themselves into volume-driven, margin-efficient positions rather than premium-revenue positions. The current generic range (28 active SKUs across OTC and Prescription) is financially sound and should be maintained or selectively expanded rather than treated as a lower-value segment of the catalogue.

Primary recommendation: Keep the generic range and use it as a margin-percentage lever, especially in Prescription category, where the margin percentage gap over branded products is widest.

**Methodology**

Data sources: Three tables from the pharmacy distributor's sales dataset: Fact Sales (62,139 transactions, Jan 2024–Dec 2025), Dim Product (220 SKUs), and Dim Pharmacy (120 stores).

Scope: Analysis is restricted to active (non-discontinued) products, since the objective is to evaluate current stocking and pricing strategy rather than historical performance.

Comparability filter: Only categories that contain both generic and branded products were included, so that generic and branded performance is always being compared within the same category rather than across dissimilar product types. This left OTC and Prescription as the two eligible categories (Medical Devices and Personal Care were excluded because they have no generic equivalent in this catalogue).

Method: Sales transactions were merged with product and pharmacy attributes, then aggregated to SKU level (revenue, margin, units sold) and further aggregated to category by generic-status level to compare averages.

Limitations: The analysis is descriptive, not causal. The differences in average revenue and margin between generic and branded products may also reflect factors not modelled here (e.g. promotional activity, pharmacy mix, launch timing). No formal significance testing was applied to the average differences reported.

**Data Findings**

Portfolio composition. Of the active, eligible-category catalogue, branded products outnumber generics in both categories:
    • OTC: 35 branded SKUs, 17 generic SKUs 
    • Prescription: 32 branded SKUs, 11 generic SKUs 
Generics make up roughly a third of OTC SKUs and a quarter of Prescription SKUs, a real but minority share of the assortment.

Per-SKU performance:

    • OTC Branded: average revenue €31,919, average margin €9,436, average units sold 3,145
    • OTC Generic: average revenue €29,450, average margin €8,682, average units sold 3,099
    • Prescription Branded: average revenue €64,210, average margin €13,955, average units sold 1,413
    • Prescription Generic: average revenue €54,084, average margin €12,177, average units sold 1,365
Generics undercut branded pricing in both categories by about 6% lower in OTC and 13% lower in Prescription. Unit volumes are close to branded levels in OTC (98% of branded units) and slightly lower in Prescription (97%), meaning generics are not compensating for the price gap through materially higher volume; the price discount is not being fully offset by demand.

Overall margin percentage. Despite lower absolute revenue and margin per SKU, generics convert revenue to margin more efficiently overall:

    • Branded: total revenue €3,171,882, total margin €776,827, margin percentage 24.49% 
    • Generic: total revenue €1,095,579, total margin €281,554, margin percentage 25.70% 
This is the central finding: generics run about 1.2 percentage points higher on margin percentage than branded products, across the combined OTC and Prescription base.

**Visualizations**

<img width="1265" height="530" alt="avg revenue per sku by category" src="https://github.com/user-attachments/assets/29118898-4e28-464b-b938-878f32675f7f" />


<img width="1484" height="584" alt="margin %" src="https://github.com/user-attachments/assets/fe4a0490-e709-46f5-8c70-2f79f0e4a617" />

<img width="1265" height="530" alt="avg margin per sku by categpry" src="https://github.com/user-attachments/assets/dc773e3f-3bf9-4fc9-956e-d6b31cb4fea7" />


**Recommendations**

    1. Maintain the generic range at current or slightly expanded levels. The margin-percentage advantage confirms generics are not a drag on profitability; they are a legitimate margin-efficient segment of the portfolio.
    
    2. Prioritise generic expansion in Prescription over OTC. The margin percentage gap over branded products is wider in Prescription than in OTC, suggesting Prescription generics convert revenue to margin more efficiently. Test additional Prescription generic listings in categories where branded penetration is currently high.
    
    3. Investigate the volume gap rather than assume it away. Generic units sold trail branded units in both categories despite comparable or lower revenue per SKU. This gap is worth a follow-up look at placement, promotion, or pharmacist substitution behaviour — a lever not tested in this analysis.
    
    4. Use margin percentage, not average revenue per SKU, as the KPI when evaluating generic performance. Reporting generics purely on revenue or margin-per-SKU understates their contribution, since it doesn't capture how efficiently that revenue converts to margin. A margin-percentage view gives category managers a fairer comparison across generic and branded products.
    
    5. Break down the margin-percentage comparison by promotional activity and pharmacy mix before acting on it. Confirming that generics and brands see similar levels of promotion and are sold through a similar mix of pharmacy types would strengthen confidence that the margin-percentage gap reflects the products themselves rather than where or how often they're discounted and sold.
    
**Appendix**

A1. Portfolio composition (all active products, full catalogue)

    • Active (not discontinued): 157 branded, 28 generic 
    • Discontinued: 30 branded, 5 generic
    
A2. Full SKU-level performance table (eligible categories only)

    • OTC Branded: 35 SKUs, total revenue €1,117,159.56, avg revenue €31,918.84, total margin €330,272.05, avg margin €9,436.34, total units 110,084, avg units 3,145.26 
    • OTC Generic: 17 SKUs, total revenue €500,653.20, avg revenue €29,450.19, total margin €147,601.69, avg margin €8,682.45, total units 52,690, avg units 3,099.41
    • Prescription Branded: 32 SKUs, total revenue €2,054,722.21, avg revenue €64,210.07, total margin €446,554.70, avg margin €13,954.83, total units 45,230, avg units 1,413.44 
    • Prescription Generic: 11 SKUs, total revenue €594,926.18, avg revenue €54,084.20, total margin €133,952.30, avg margin €12,177.48, total units 15,015, avg units 1,365.00
    
A3. Data sources

    • Fact Sales.csv: 62,139 transaction records, Jan 2024–Dec 2025 
    • Dim Product.csv: 220 products, includes ListPriceEUR, IsGeneric, Category, Brand 
    • Dim Pharmacy.csv:120 pharmacy locations across multiple European countries 

A4. Notebook reference Source analysis: Generic vs Brand Analysis.ipynb


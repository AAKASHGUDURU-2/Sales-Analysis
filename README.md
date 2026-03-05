# Sales-Analysis: Strategic Performance Audit

## Project Overview
Analyzing nearly 50k orders of an American eCommerce company exporting Furniture, Technology, and Office Supplies globally. I performed a detailed Exploratory Data Analysis (EDA) of their sales, beginning with data cleaning by removing the Postal Code column (redundant due to international export nulls). The core objective was finding MoM Growth and Profit Margin % overall and per category, identifying trends, and visualizing them in a Tableau dashboard. I also analyzed the correlation between MoM Growth and Profit Margin % and identified every negative profit month.


##  Project Steps

1.  **Data Cleaning**: Finding null values and dealing with them; dropping the Postal Code column as it is not required for EDA.
2.  **Date Management**: Analyzing monthly data by ensuring the Date column is in the Datetime datatype and converting it to Month periods.
3.  **Sales & MoM Growth**: Identifying best and worst months. Finding that "Sales Season" for Furniture and Technology peaked in January (variable by year), likely driven by "Back to School" or refreshes.
4.  **Volatility Analysis**: Calculating Standard Deviation per category to find risk. Finding that peak seasons often occur in August due to academic cycles.
5.  **Trend Identification**: Using line graphs to find January’s negative MoM growth (-66.25%), concluding this happens annually after essential holiday/school shopping ends.
6.  **Profit Margin Analysis**: Using ($Profit / Sales$) to understand if sales growth is translating into actual profit.
7.  **Category Deep-Dive**: Analyzing MoM Growth and Profit Margin % (Max, Min, Mean) to see money saved after marketing and discounts.
8.  **Performance Tracking**: Identifying the best and worst performing months for targeted business review.


##  Negative Profit Month Audit
Through Python filtering and Tableau Heatmap visualization, I identified critical periods where the company operated at a loss:

* **Furniture**: Hit a record low Profit Margin of **-4.38%** in January 2012.
* **Identified Risk**: Total months with negative profit were tracked to pinpoint structural inefficiencies in discounting during low-demand months.


## 🧠 Things I Have Learnt

1.  **Encoding Scripts**: Always mention the encoding script if it is not the Jupyter default to ensure data portability.
2.  **NULL Value Handling**: Learning when to drop data; since city names were present, Postal Code was not necessary for geographic analysis.
3.  **Pandas Mastery**: Utilizing `.pct_change()` for efficient growth tracking.
4.  **Financial Metrics**: Understanding that Profit Margin = Profit / Sales is the true measure of efficiency.
5.  **Granular Analysis**: Recognizing that category-level profit margins provide much deeper details than overall company averages.
6.  **Transformation Strategy**: If working with a summarized table, use the **Split, Apply, and Combine** strategy instead of re-aggregating to maintain data integrity.
7.  **Date Concepts**: Identifying the need to master complete Date-related concepts for time-series accuracy.
8.  **Comprehensive Auditing**: Learning to combine monthly sales growth, category max/min, standard deviation, and correlation analysis to find negative profit months and structural risks.


## Strategic Recommendations

* **Re-evaluate Furniture Discounting**: Since Furniture showed a negligible **0.014 correlation** between growth and profit, aggressive discounting to drive volume should be curtailed, especially in January.
* **Capitalize on Office Supplies**: With a higher scaling potential (**0.201 correlation**), marketing budgets should be shifted here to maximize profitable growth.
* **Stabilize January Operations**: Implement inventory clearing in December to avoid the massive **-66.25% growth crash** and negative margins observed every January.
* **Focus on Technology**: Maintain the high efficiency (**13.82% mean margin**) of this category as it acts as the primary profit stabilizer for the company.


## Dashboard Results
* **Sales Growth vs. Profit Margin Trends**: Visualizing the "efficiency gap".
* **Monthly Profitability Heatmap**: Pinpointing the -4.38% Furniture crash in Jan 2012.
* **Category Correlation**: Proving the 0.014 vs 0.201 relationships visually.

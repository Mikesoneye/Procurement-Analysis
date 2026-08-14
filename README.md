# Procurement performance and spend analysis
## Project Overview
This project analyzes procurement performance to provide insights into purchasing activity, spending patterns, purchasing officer performance, receiving departments, account types, and purchase order billing status.

The analysis was designed to help stakeholders understand where procurement spend is concentrated, how purchasing activity changes over time, which purchasing officers contribute most to procurement spend, and where potential procurement management opportunities exist.

Key areas explored include:

- Purchasing officer performance
- Purchase order (PO) value and volume
- Procurement spend by receiving department
- Procurement spend by account type
- Monthly and quarterly purchasing trends
- Purchase order billing and receipt status
- Factors associated with differences in purchase order value

## Key Abbreviation
  PO - Purchase Order

## Business Questions
- Which purchasing officers contribute the most to procurement spend?
- Which departments account for the largest share of PO value?
- Which account types drive procurement activity?
- How does procurement activity change throughout the year?
- What proportion of PO value is billed, pending billing, or pending receipt?

## Data Source

The dataset was sourced from a Senior colleague who shared it on LinkedIn and was downloaded as xlsx file. The dataset contains 100,000 rows and 14 columns, including information on:

- Purchase Order
- Purchasing Officers
- PO Amount
- PO Date and other procurement-related attributes

## Tools Used
Power BI — Data transformation, data modeling, DAX calculations, and data visualization

## Data Preparation and Cleaning

The dataset was imported into Power BI and prepared for analysis.

## Data Transformation

- The following date fields were converted from DateTime to Date:

`PO Date`  and `PO Modified Date`. This ensured that the date fields were appropriate for daily and period-based analysis.

- Date Table

A dedicated Date Table was created to support time-based analysis and Power BI time-intelligence calculations.

The Date Table includes:

`Date`
`Year`
`Quarter`
`Day`
`Month name` and `Month`

The table was formatted using a standard Date data type and connected to the procurement data using the appropriate date field.

<img width="682" height="331" alt="Capture" src="https://github.com/user-attachments/assets/0c5f3985-772b-4bd7-aacf-08f1588e0096" />

- Data Modeling

A dimensional data model was created by connecting the Date Table to the Procurement Data fact table using a one-to-many (1:*) relationship with a single cross-filter direction. This structure supports consistent filtering and time-based analysis across the dashboard.

<img width="841" height="488" alt="Capture" src="https://github.com/user-attachments/assets/9e165670-6ced-4ff2-8722-2e46271dbdc8" />

## DAX Measures

Several DAX measures were developed to calculate key procurement performance indicators and support the analysis.

Examples include:
- Total Purchase order value
<img width="372" height="84" alt="total Purchasing Order" src="https://github.com/user-attachments/assets/1da88de6-4e46-4fb8-ae22-7c5b8dda2ec8" />

- Purchase Order value by Purchasing Officers
<img width="852" height="83" alt="PO contribution by purchasing officers" src="https://github.com/user-attachments/assets/a89fb7d6-214a-4c8a-a7df-c8147518c218" />

- Purchase Order value by Receiving Department
<img width="889" height="79" alt="PO contribution by receiving department" src="https://github.com/user-attachments/assets/522dc1cb-ad82-4941-a082-a13bdd21ecb7" />

- Purchase Order value by type of account
<img width="828" height="101" alt="PO contribution by type of account" src="https://github.com/user-attachments/assets/95779cc7-42a2-4484-ab33-c35d06b9a909" />


## Key Findings
1. **Purchasing Officer Performance**: Fyodor Dostoyevsky was the highest-contributing purchasing officer based on PO savings amount and PO amount across both domestic and international purchasing activities. Fyodor accounted for approximately 20% of domestic purchasing order value and 14% of international purchasing order value. In contrast, Aldous Huxley had the lowest contribution across both domestic and international purchasing activities, accounting for approximately 1% in each category. This indicates a significant concentration of purchasing activity among certain purchasing officers.
<img width="451" height="339" alt="Capture" src="https://github.com/user-attachments/assets/59ee77de-86f5-4ec3-8503-4c9dec7407f6" />
<img width="793" height="304" alt="Capture 1" src="https://github.com/user-attachments/assets/9de92750-e248-4f7d-be3d-1a5cadb104ed" />

2. **Quarterly Procurement Trend**: Purchase order value increased progressively from Quarter 1 through Quarter 4. This suggests that procurement activity was highest toward the end of the year and may indicate increased purchasing requirements, budget utilization, or operational demand during the later quarters.
<img width="265" height="178" alt="Capture" src="https://github.com/user-attachments/assets/3f1c9695-7bdf-4caa-b11d-22a0bd7687cb" />

3. **Monthly Purchasing Activity**: September recorded the highest number of purchase orders, while February recorded the lowest. This indicates that procurement activity was not evenly distributed throughout the year, with purchasing activity becoming considerably stronger later in the year.
<img width="190" height="266" alt="Capture" src="https://github.com/user-attachments/assets/aeb810ad-839a-4530-8b62-76b7c52c4f9f" />

5. **Account Type Concentration**: Travel & Entertainment represented 33.41% of purchase order activity, followed by Office & Supplies at 26.89%. Together, these two account types accounted for approximately 60% of purchasing activity, indicating a high concentration of procurement across a relatively small number of spending categories.
<img width="443" height="311" alt="Capture" src="https://github.com/user-attachments/assets/f6c8d59e-fba5-4e49-90ce-4e266ad11dc4" />
<img width="486" height="235" alt="Capture 12" src="https://github.com/user-attachments/assets/07bc7b98-6002-4746-bb47-dde5a5d90809" />

6. **Transaction and billing Status**: Approximately $76.36 million of procurement spend was fully billed, indicating that the majority of purchase order value had progressed to the billing stage. However, approximately $7.02 million remained pending billing, while approximately $2.20 million was associated with pending or partial receipt. These outstanding amounts represent areas that may require follow-up from procurement, receiving, and finance teams.

<img width="351" height="272" alt="Capture 14" src="https://github.com/user-attachments/assets/4aeab93a-395f-40d9-8cda-43b94964d928" />

7. **Procurement Spend by Department**: Marketing accounted for the largest share of purchase order value at approximately $34.28 million (39%), followed by G&A at $28.49 million (33%). When Technical is included, these three departments accounted for approximately 92% of total purchase order value. This indicates a significant concentration of procurement expenditure among a small number of departments.
<img width="535" height="232" alt="Capture marketing" src="https://github.com/user-attachments/assets/c4c4d4b4-ecc3-4c8a-b57e-ad99e64fb53f" />


## Recommendations
1. **Review Procurement Workload Distribution**

The significant difference in procurement contribution between purchasing officers suggests that procurement workload may not be evenly distributed. Management should review purchasing officer workloads, responsibilities, and purchasing categories to determine whether high-performing officers are carrying disproportionate procurement volumes.

2. **Monitor Departmental Spending Concentration**

Marketing, G&A, and Technical departments account for approximately 92% of total PO value. These departments should therefore receive greater attention during procurement budget reviews. Management should monitor actual PO spending against budget to identify unusual increases or potential cost-control opportunities.

3. **Address Pending Billing and Receipt Items**

The $7.02 million pending billing and $2.20 million pending or partially received should be investigated. Procurement, receiving, and finance teams should establish a regular reconciliation process to identify delayed invoices, partially received orders and supply related delays.

4. **Review High- and Low-Performing Purchasing Officers**

The difference between purchasing officers should be investigated to understand whether it is driven by: Different purchasing responsibilities, Purchase volume, Supplier relationship.

5. **Investigate High-Value Spending Categories**

Travel & Entertainment and Office & Supplies together account for approximately 60% of purchasing activity. Management should review these categories to identify opportunities for spending limits, volume-based discounts and improved procurement policies. Reducing unnecessary spending within these high-volume categories could have a meaningful impact on overall procurement efficiency.

## Limitations
- The dataset covers only one year (2014), which limits the ability to perform year-over-year analysis.
- The single-year timeframe also makes it difficult to determine whether the observed monthly and quarterly patterns represent recurring seasonal trends or are specific to 2014.

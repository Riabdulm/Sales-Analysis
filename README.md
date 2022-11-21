# Sales-Analysis
Regional Sales Analysis of a retail company based in the United States

## Introduction:
The company is a retail company located in the United States. For anonymity, the company will be assigned the name RegSales Co for this project. RegSales Co has stores in all the states in the US with a presence in Cities, Towns and Boroughs. The company stores in these locations have been grouped into four regions which consist of Northeast, West, South and Midwest.

RegSales co-management team engaged a financial analyst to analyse their performance across these regions and also know who their standout sales team, customers, products, and which channel is the best for promoting and selling their products. This is aimed to help the company maximize the opportunities in the market and further cause disruption to their competitors in the retail market.


## Objectives of the Analysis:
The objectives of the analysis are listed below:
 
    i.	What region is the best performing region in terms of profit (Gross profit) 
  
    ii.	To know the customer’s top profitable customers and be able to focus on them to avoid losing them to competitors
  
    iii. To know what the most profitable products are among the products they are selling 
  
    iv.	To understand which sales channels work best in the different regions

These insights will be used by the company’s key stakeholders – current shareholders, management team, potential investors, and employees to make value-adding decisions for the organization and its customers across the US.


## Data Sourcing and Preparation:
The data is publicly available, and it is located at - https://data.world/dataman-udit/us-regional-sales-data. The available sales data for RegSales Co is for June 2018 to January 2021. 

### Data Processing: 
For the data to help answer the questions being asked and the objectives of this project, several tables will have to be joined together. The data consists of 7,991 sales completed during this period. The main data is located in the regional_sales_data table which has 17 columns. However, other information such as customer_name, product_name, population, and region of the stores are needed from the other four tables in the dataset.

**Tools used** include SQL and Tableau

### SQL:

From the first table, only 8 columns were needed to contribute to the analysis, therefore only these 8 columns were selected from the regional_sales_data table. The other columns needed were joined together to this table using inner joins. Inner Join was used because not everything in the first table was needed. 

The following are the steps taken by SQL to clean and process the data.

  •	Use customerID to bring in customer_name from the Customers sheet

  •	Use productid to bring in the product_name from the product sheet

  •	storeID to return the population from the store location sheet 

  •	Use SalesTeamID to bring in the region from Sales Team Sheet
  
  •	Check for NOT NULL to ensure empty data are not joined/imported from the tables
  
  •	Then ORDER BY store_ID.

**SQL queries** are contained here --------> https://console.cloud.google.com/bigquery?sq=925461410871:80dbae7ababe45bb8da1f985924f2272 

### Tableau:

  •	Data is then exported to CSV to be analysed on Tableau
  
  •	Checked data types on Tableau to ensure it is the correct data types and formats 
  
  •	Created charts and dashboards to visualize and analyse the data to reach appropriate conclusions and make recommendations based on the business objectives.

The **interactive Dashboard created on Tableau** can be found here --------> https://public.tableau.com/app/profile/ridwan.abdulmumeen/viz/USRegionalSalesAnalysis_16689160412780/Dashboard1 


## Findings: 
  **i.	Most profitable region**: The Midwest is the most profitable region with $8.92m in gross profit over this period (June 2018 to January 2021). And    the South is the least profitable with $6.80m.

  **ii.	Best customer in terms of Gross Profit**: Filtered for the top 10 most profitable customers. Medline is RegSales Co's most profitable customer with the company making a gross profit of $852,170 from them during this period.

  **iii.	Products’ gross profit**: The most profitable product is Accessories with appx $909m gross profit made from them. Cocktail glass is second with approximately $769m in gross profit. However, the least profitable product is Pillows with approximately $464m.

  **iv.	Sales channel performance by region**: In the Midwest, Distributorship is the most popular sales channel. Moreover, no sales were made in this region via Wholesale in the period. The Northeast saw most of its sales (58%) In-store, with Online sales coming a distant second. The South had most of its sales online, and In-store came a close second. The West had the majority of its sales In-store, and the least sales were via Distributorship.


## Conclusion & Recommendations:
  **i.**        The Midwest is the most profitable region, and the region also had the highest sales during the period with approximately 29% of the total ordered quantity. This might be due to the Sales team in that region working hard and pushing sales. It might also be that the company’s competitors in this region are not as strong as those in other regions. 

**Recommmendation:** The company should monitor their performance in this region keenly as this is RegSales Co’s cash cow, and it will need the cash flows from there to invest in other regions like the South or Northeast that are not performing as well.


  **ii.**       Medline is RegSales Co’s most profitable customer with Apotheca, Ltd coming a close second. These two customers purchase the company’s products across the four regions. 
		
**Recommmendation:** The company should ensure to keep these two customers and the other profitable customers satisfied. Reward programs and discounts can be offered to them to ensure they stay loyal and do not get poached by their competitors. This will also help the company avoid the acquisition cost of trying to lure newer customers.


**iii.**        Accessories being the most profitable product might be because of their versatilities as accessories are needed for lots of things. On the other hand, the pillows are the least profitable. 
	
**Recommmendation:** RegSales Co. should keep on selling pillows as they might be bought together with other complementary products the company is selling such as Bedroom Furniture, Blankets, Furniture cushions etc.


  **iv.**       The most popular sales channel for the company during this period was In-store with 41% of the company sales going through this channel. The least popular sales channel is Wholesale with 11%. However, different sales channel has worked well in different regions of the country for the company. 
  
**Recommmendation:** The company should maximize the sales channel that best suits a particular region. Other sales channels should also be explored so the company can have a competitive advantage over their competitors in the region.

A comprehensive report of the analysis is given on **PowerPoint slides**, and it can be found here ---------> https://github.com/Riabdulm/Sales-Analysis/blob/9f0c3a815381c65122560aa8275630d321bd5a2f/PowerPoint%20Presentation%20of%20RegSales%20Co.%20Regional%20Sales%20Analysis.pptx 


## Additional Analysis / Limitations of Current Data:
  •	No complete month’s information for all the years June 2018 (only 7 months) – January 2021 (one month only). So, we cannot compare monthly performance to see the trend as the data is not complete for all the months in the 4 years. Doing this will create bias in the results as the data is incomplete.
  
  •	Unable to calculate the net profit of RegSales Co during this period because there are no data on other costs such as adverts, administrative expenses, fixed costs etc. 
  
  •	Not enough data to further analyse complementary products that are purchased together to advise the company on which products to discontinue selling due to its profitability.

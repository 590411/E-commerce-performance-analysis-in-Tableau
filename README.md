# E-commerce-performance-analysis-in-Tableau
Calwest E-Commerce analysis using Tableau


## Company activity/ field : sells health-conscious products for people and their pets
 

## Table of Content
-  [Project Overview](#project-overview)
-  [Data Sources](#data-sources)
-  [Tools](#tools)
-  [Preparation](#Preparation )
-  [Findings](#findings)
  
### Project overview
---

---- **Company information**

    -Calwest E-commerce is a company that sells health-conscious products for people and their pets
 

---- **Delivrables**

    -Build two dashboards  that will help summarize high level company data and regional performance
 	  - Create the data model
	  - Create a dashboard to analyse E-Commerce performance
	  - Create a dashboard to  analyse performance location
	  - Add interactivity to dashboards

![5](https://github.com/user-attachments/assets/f4cff69b-3db1-4738-830c-4cdd7138462f)


 ### Data sources
 ---

*Company  Data  ,the dataset use for this analysis is from the factOrder csv file and other dimension tables . we have data on cost, units , quantity ,revenue ...*

### Tools
---
  - Excel 
  - Tableau

### Preparation
---
  -Fact table : factOrder
	-Dimension tables : dimCustomer , dimLocation , dimPayment , dimProduct , dimPromo , dimShipping

 	All the Dimension tables  has been joint to Fact table  using relationships instead and not joins

 	The performance/cardinality options between Fact table and Dimension tables are many(Fact table) to one ( Dimension tables )

 	The referential integrity  options between Fact table  and Dimension tables are   "all records match(Fact table)" and "all records match ( Dimension tables )" .But for the relationship between   Fact table and the dimPromo  table is  "some records match(Fact table)" and "all records match ( dimPromo  )" , as not all orderId  had a discount/ promo .

  To build our analyse E-Commerce performance dashboard , we need to compute the following metrics

		*Profit :: SUM([Revenue])- SUM([Cost])
		*Gross Revenue :: SUM([Revenue])
		*Profit Margin %:: [Profit]/[Gross Revenue]
		*Profit Margin % – Row Level :: ([Revenue] - [Cost]) / [Revenue]
		*Discount :: SUM([Base Revenue])-[Gross Revenue]
		*Quantity :: SUM([Quantity])
		*Units  :: SUM([Units])
		*DISTINCT COUNT of OrderID :: COUNTD([Order ID])   
		*DISTINCT COUNT of Customers  :: COUNTD([CustomerId])
		*AVERAGE Order Value ::  [Gross Revenue]/[Order Count]

  Dashboard 1 - To build the High Level Performance Dashboard : I have created the below charts
		* Line chart
		* Bar chart
		* Scatter chart
		* Bans

### Findings
---
  *What is the Gross Revenue total in the dataset? Base on the BANS , the total gross revenue is $81.27M
	*What is the overall Profit % in the dataset?  Base on the BANS , the  overall profit % is 54.35% 
	*What is the profit for fact Order RowID 189787? the profit for RowID 189787 is 0.4617
	*What is the Order Value Avg for the whole dataset ?  Base on the BANS , Order Value Avg is  $440.79
	*What is the total units for 2021 only? By slicing , the total unit for 2021 is 3.32M
	*What is the profit margin of the highest revenue product, in 2021? By slicing ,Sneaky Protein Bar is the product with the highest revenue ,it profit margin is 0.9467
	*What is the Gross Revenue for pet Food in July 2021. By slicing , the  Gross Revenue for pet Food in July 2021 is $1446837
 

 

💻💻  



# BI 360---ATLIQ HARDWARE SALES REP0RT
Live Report Link:https://app.powerbi.com/groups/me/reports/5363c89e-3140-422f-ba29-e67684c0aef0/fc9c2f0e40aa0907c1c0?experience=power-bi
## Project overview
AtliQ Hardware has experienced rapid growth in recent years and has decided to implement data analytics using PowerBI for the first time. 
This initiative aims to outpace their competitors and make data-driven decisions. The project is expected to address stakeholders' questions across various aspects such as
finance, sales, marketing, and supply chain.
## Company’s back ground
AltiQ hardware is a company which has grown vastly in the recent years, and opened business all over the globe. It is a company which sells, computer and computer accessories through three mediums/channel
* Retailers
* Direct
* Distributors
Recently the company has faced a unforeseen loss by opening store in America based on the surveys, intuition and some excel analysis and also the company’s competitors has handful of analytics team to perform analysis and make data driven decision. So, the AltiQ hardware has no other option other than building their analytics team for data driven insights and decisions in the future to survive better in the industry.

## Tech Stacks

* SQL
* PowerBi Desktop
* Excel
* DAX language
* DAX studio (for optimizing the report)
# Power BI Tools and Techniques Learned
* What are all the questions should be asked before staring the project
* Creating calculated columns
* Data modeling
  * Primary Key
  * Foreign Key
* Ceated measures using DAX language
     * Learned the importance of **Row Context, Filter Context and Context transition**.
     * DAX functions used :-
        * MAX()
        * SUM()
        * CALCULATE()
        * RELATED()
        * ALLNOBLANKROW()
        * SAMEPERIODLASTYEAR()
        * UNION() & ROW() FUNCTION
        * HASONEVALUE()
        * SWITCH() function to create conditional measure.
        * Used DATE FUNCTION & MONTH FUNCTION for creating **calculated columns**.
        * SELECTEDVALUE()
        * ISFILTERED()
        * ISCROSSFILTERED()
  
*  Created dynamic calculated column to give YTD/YTG based on the last sales date.   
* Using Bookmarks to switch between two visuals
* Page navigation with buttons
* Using divide function to prevent zero division errors
* creating date table using m language in Power Query Editor.
* Dynamic titles based on the applied filters.
* Using KPI indicators
* Conditional formatting the values in visuals using icons or background color
* Using Fields parameters. Fields Parameters allows users to choose which column to use to slice and dice values in a Power BI visual. 
* Data validation techniques
* PowerBi services
* Publishing reports to PowerBi services
* Setting up personal gateway to set up the auto refresh of data
# Business related terms
* Gross price
* Pre-invoice deductions
* Post-Invoice deductions
* Net Invoice sale
* Gross Margin
* Net sales
* Net profit
* COGC - cost of goods sold(Includes Mmnaufacturing cost,Freight cost and other cost)
* YTD - Year to Date
* YTG - Year to Go
Direct
Retailer
Distributors
Consumer

## Dataset Understanding.
Understanding what data is available will be more helpful while doing analysis. before jumping on to the analysis get good understanding of what are data available.

 Dimension table : It will have the static data like details of customer and products

 Fact table : It will have the data about the transactions

  ### Database -gdb041:
 * dim_customer
   * 27 distinct markets (ex India, USA, spain)
   * 75 distinct customers thorough out the market
   * 2 types of platforms
   * Brick & Motors - Physical/offline store
   * E-commerce - Online Store (Amazon, flipkart)
   *Three channels
    * Retailer
    * Direct
    *  Distributors
 * dim_market
   * 27 distinct markets (ex India, USA, spain)
   * 7 sub-zones
   * 4 regions
     * APAC
     * EU
     * nan
     * LATAM
* dim_product
  * Divisions
      * P & A
        * Peripherals
        * Accessories
      * PC
        * Notebook
        * Desktop
      * N & S
        * Networking
        * Storage
  * There are 14 different categories, Like Internal HDD, keyboard
  * There are different variants available for the same product
* fact_forecast_monthly
   * This table is used to forecast the customer’s need in advance, which can help in
     * Higher customer satisfaction
     * Reduced cost in warehouses for storage purpose
   * The table is denormalized by data engineering team, as it is a data warehouse which is aimed to be used for analytical work.
   * All the date of the month will be replaced by the start date of the month
   * It will have all the column names and in the end it will have the forecast quantity need of the customer
* fact_sales_monthly
  *This table is more or less is same as fact_forecase_monthly table, but the last column has the value of sold quantity instead of forecast value.
### Database- gdb056
 * freight_cost
   * This table has details of travel cost and other cost for each market with fiscal year
 * gross_price
   * Has the details of gross prices with product code
 * manufacturing_cost
   * Has the details of manufacturing cost with product code with year
 * Pre_invoice_dedutions
   * Has the details of pre invoice deductions percentage for each cutomer with year
  * Post_invoice_deductions
 *Post invoice deductions and other deductions details
## Importing data into PowerBi
As the database is MySQL in this project, we need to import the datasets from Mysql database to PowerBi by providing the Database access credential.

## Data Model
![Screenshot 2024-05-28 120506](https://github.com/Sidsharma11/Atliq_sales_report/assets/167175484/79bca9f1-066e-490f-8efa-6532cb16fb70)



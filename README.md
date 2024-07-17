# Sales insight (power-bi)
Sales Insight of an Online Store in Europe Using (POWER-BI)

# Sales-Dashboard


## Problem Statement

This dashboard helps the Business understand their customers And Sales better. It helps the Business know how their Sales in Various Regions and  Categorise are Expanded. Through different Buying Patterns, they get to know their improvement area, & thus they can improve their Products by identifying these area. It also lets them know the  Orders & Category Sales, thus since by using this dashboard they have identified this Queries and they can further work on factors responsible for these unwanted Losses.

Since, Amount Of Sales from North (~22%), South (~19%) and Central (59%) While ,

 The Profit share from North (~29%), South (~12%) and Central (59%).

Thus can clearly see even while
the sales are high the profit % is Way less in South Region Comparatively
the sales and the profit % in the North, Central Regions are Great,

 thus in all they must work on improving their services and profits in the South Region. 



### Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is a Excel file.
- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
- Step 3 : Also since by default, profile will be opened only for 1000 rows so you need to select "column profiling based on entire dataset".
- Step 4 : It was observed that in none of the columns errors & empty values were present except column named "Discount".

- Step 5 : For calculating Profit, null values were not taken into account as only less than 1% values are null in this column(i.e column named "Profit") 
- Step 6 : In the report view, under the view tab, theme was selected.
- Step 7 : Since the data contains various Categories and Sub-Categoriess, thus in order to represent Sales, a new visual was added using the Stacked Column Chart in the visualizations pane in report view. 
- Step 8 : Visual filters (Slicers) were added for Two fields named "Date" , "Region", 
- Step 9 : Four card visuals were added to the canvas, one representing "Sum_of_Sales" ,"Total_Profit & other representing "Order_Quantity" in Count.
           
           Although, by default, while calculating average, blank values are ignored.
- Step 10 : A Pie chart was also added to the report design area representing the Profit($) by Region & Donut Chart to Represent Sales By Region.                

- Step 11 :Matrix Visual was Created for Identifying The Top 10 Customers Via Sales;

  
In our dataset, Some parameters were assigned value 0, representing those parameters are not applicable for some customers.

All these values have been ignored while calculating "Discount" for each of the parameters mentioned above.

- Step 12 : And Another Dashboard Was Created for identifying the differnent sales insights for each categoery and sub-category.

- Step 13 : Inserted Two slicers for Identifying And Getting Valuable Inights for each Category and Sub-Category.

- Step 14 : "Discount_given"

for creating new column following DAX expression was written;
       
        Discount_Given($) = if('Order Breakdown'[Discount(%)]>0,('Order Breakdown'[Discount(%)]*'Order Breakdown'[Sales($)]),0)
        

 # Report Snapshot (Power BI DESKTOP)

 ![Screenshot 2024-07-16 232520](https://github.com/user-attachments/assets/e2aa3fc2-fd96-4a2c-9b6c-dcab5d4c15e5)
 
![Screenshot 2024-07-16 232545](https://github.com/user-attachments/assets/13e8dea4-0814-46f5-bbb9-ef94c3702271)

# Insights


Following inferences can be drawn from the dashboard;

### [1] Sales Demographics

   Number of Customers = 4.117 k 

   Number OF Orders = 8.047 k

   Amount Of Sales = 2 Mil 

  Total Amount of Profit = 283 k
           
### [2] Customer Demographics

    Northern Europe = 4.427 k 
  
    Central Europe =  4.427 k

    Southern Europe = 1.81 k
  
  ### [3] Shipping Demographics
    
    Amount Sales by Region :-
    
    Economy = 1413 k 

    Economy Plus = 484 k

    Priority = 320 k

    Immediate = 131 k

  Insight - Economy ,Economy Plus contributes to ~81 % of sales ,
  while Immediate Mode,Priority contibutes Contributes way less ~19 %



      
 ### [4] Some other insights
 
 ### Category Sales
 
 1.1) Office Supplies Gains The Most Count of  Sales i.e 19.9 k which is 824 k in Amount Of Sales.
 
 1.2) Technology Assigns of 5.8 k  number of Sales and gives the highest 886 k Amount Of Sales.

 1.3) While Furniture Contributes with 4.6 k in num of sales and 639 k in Amount of Sales
 
         -thus, maximum customers Purchase Office Supplies Via the store.
 
 ### Sub-Category
 
 2.1)  While Art is the Most Selling in Sub-Category at 4.3 k it assigns 127 k of Amount in Sales
 
 2.2)  The top 3 selling Products in the Sub-Category are Arts , Binders And Storage .
 
 2.3)  While the Most Profitable Products are Appliances , Arts and Storage.
 
 
         - Tables are The Most Loss making product.
         
 ### Over-All Inights

* The Discount_Amount and Total Units Sold of Tables is Leading to a Overall loss of 20.7 k $.

* While Book Cases contributes The Most Amount of Profit Its Sales is Limited to 1.43 k units.

* The Northen Europe sales to profit Ratio is low and the Southern Europe in way lower as Compared to the Central Region.

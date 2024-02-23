# Addidas Sales Analysis

### Dashboard Link : https://app.powerbi.com/groups/me/reports/384d017e-e935-44dc-9e7d-1626c1a36de1/ReportSection

## Problem Statement

This dashboard helps the Addidas company to understand their customers better. It helps the company know if their customers are satisfied with their services. Through different Operating details, they get to know their improvement area, & thus they can improve their services by identifying these area. It also lets them know the average unit sold & total sales, thus since by using this dashboard they have identified this problem, they can further work on factors responsible for these to improve sales as per regions.

### Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is a excel file.
- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
- Step 3 : Also since by default, profile will be opened only for 1000 rows so you need to select "column profiling based on entire dataset".
- Step 4 : It was observed that in none of the columns errors & empty values were present except column named "City" and "Gender".
- Step 5 : For calculating most profitable category, null values were not taken into account as only less than 1% values are null in this column(i.e column named "Gender") 
- Step 6 : Visual filters (Slicers) were added for three fields named "Invoice Date", "Product" & "State".
- Step 7 : Five card visuals were added to the canvas, representing total sales in 2021, total sales in 2021, Total Customers, most profitable category and total unit sold.
           Using visual level filter from the filters pane, basic filtering was used & null values were unselected for consideration into average calculation.
           
           Although, by default, while calculating average, blank values are ignored.
- Step 8 : A bar chart was also added to the report design area representing the number of satisfied & neutral/unsatisfied customers. While creating this visual, field named "Gender" was also added to the Legends bucket, thus number of customers are also seggregated according the gender. 
  
In our dataset, Some parameters were assigned value 0, representing those parameters are not applicable for some customers.

- Step 9 : In the fourth page in stacked column chart, analysed sales and profit by month per a year.
- Step 10 : Calculated column was created in which, customers were found most profitable and valuable category.

for creating new column following DAX expression was written;
       
        Most Profitable Category = CALCULATE(MAX('Data Sales Adidas'[Product]))
	Most Valuable Category = MAX('Data Sales Adidas'[Product])
        
- Step 11 : New measure was created to find total count of customers.

Following DAX expression was written for the same,
        
        Count of Customers = COUNT('Data Sales Adidas'[Retailer ID])
        
A card visual was used to represent count of customers.

![image](https://github.com/SD739/Test/assets/160561275/fee84a9e-c012-432b-8aec-fefdb130c1ef)
    
A card visual was used to represent this total sales.

![image](https://github.com/SD739/Test/assets/160561275/12059434-e684-436e-bbc1-0d22a61ba264)

A card visual was used to represent this total profits.

![image](https://github.com/SD739/Test/assets/160561275/58851d14-6f79-44b9-8065-3ab79c84fcf8)

A card visual was used to represent this total unit solds.

![image](https://github.com/SD739/Test/assets/160561275/7d6596a3-d09f-45a0-b92b-b1f43c22b86d)
 
 - Step 12 : The report was then published to Power BI Service.
  
https://app.powerbi.com/links/I4hD8Ab8Yi?ctid=06ed56c9-9f72-4bab-be52-871af76a1ba8&pbi_source=linkShare

# Snapshot of Dashboard (Power BI Service)

![image](https://github.com/SD739/Test/assets/160561275/f4e4041c-92d8-44e4-92d2-035d901dbed2)

 
 # Report Snapshot (Power BI DESKTOP)

 
![image](https://github.com/SD739/Test/assets/160561275/39082e50-52e6-4d91-bb6c-99fb513e3b91)

# Insights

A single page report was created on Power BI Desktop & it was then published to Power BI Service.

Following inferences can be drawn from the dashboard;

### [1] Total Number of Customers = 8346

   Total unit sold by Customers = 2 M
   
   Total sales by Customers = 717.82 M

   Total profits by Customers = 268.72 M
  
  ### [2] Sales by Retailer
  
    Sum of total sales by West Gear - 27%

    Sum of total sales by Sports Direct - 20.28%

    Sum of total sales by Amazon - 8.63%

    Sum of total sales by Foot Locker - 24.46%

    Sum of total sales by Kohl's - 11.35%

    Sum of total sales by Walmart - 8.29%

	thus, product sales rate is less with AMAZON and WALMART.

 ### [3] Total sales by Product

    Sum of total sales by Street Footwear - 37.83%

    Sum of total sales by Apparel - 33.62%

    Sum of total sales by Atheletic Footwear - 28.54%
         
 ### [4] Total profit by Product

    Sum of total profits by Street Footwear - 38.37%

    Sum of total profits by Apparel - 34.4%

    Sum of total profits by Atheletic Footwear - 27.23%

	thus, Atheletic Footwear sales and profit margin is less than other product.

 ### [5] Total profit by Gender

    Sum of total profits by Male and Female - 144.83 M and 123.9 M

       thus, more male customers satisfied than female customers.

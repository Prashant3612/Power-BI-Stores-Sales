# Store Sales Dashboard

## Problem Statement

This dashboard helps the Store to understand their customers better.This dashboard aims to consolidate and visualize two years of sales data, enabling stakeholders to gain a deeper understanding of our sales performance across various metrics. By focusing on key performance indicators (KPIs) such as total orders, sales revenue, profits, and average shipment date, the dashboard will provide actionable insights to inform strategic decision-making at all levels of the organization.

In this case we have considered the sales data of 2 years(2019,2020) in the USA.

### Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is a csv file.
- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
- Step 3 : Also since by default, profile will be opened only for 1000 rows so you need to select "column profiling based on entire dataset".
- Step 4 : It was observed that in none of the columns errors & empty values were present except column named "Returns".
- Step 5 : In column "Returns" value "#N/A" was replaced with 0. 
- Step 6 : In the report view, under the view tab, theme was selected.
- Step 7 : Three Dough nut charts were added representing "sales by payment mode", "Sales by Region" and "Sales by Segment".
- Step 8 : Visual filters (Slicers) were added for regions :"Central", "East", "West", "South" for better understanding.
- Step 9 : Four card visuals were added to the canvas, representing KPIs: Orders, Sales, Profit, Shipment Days.
- Step 10 : Three bar charts were also added to represent the "Sales by Ship Mode", "Sales by Category", "Sales by Subcategory"
- Step 11 : Two Stacked area charts were added to show monthly year on year profit, and Sales by Month in both years.
- Step 12 : Map was also added to show the sales profit contribution by states. 
  
- Step 14 : Calculated column was created in which, Delivery date was calculated from column "Order Date" and "Ship Date"

for creating new column following DAX expression was written;
       
        AvgDeliveryDays = 
        
        DATEDIF('SuperStore_sales'[Order Date]', 'SuperStore_sales'[Ship Date], DAY)
        

 # Report Snapshot (Power BI DESKTOP)

 
![Dashboard_upload](https://github.com/Prashant3612/Power-BI-Stores-Sales/blob/main/Stores_Sales_Dashboard.jpg?raw=true)

# Insights

A single page report was created on Power BI Desktop.

Following inferences can be drawn from the dashboard;

### [1] Total Number of Oders = 22K
        Total Sales: 1.6Million
        Total Profit: $175.3K
        Average shipment days: 4 
    
           
### [2] Shipment Mode
    a) Standard Delivery (176.21K): Most commonly chosen, balancing cost and speed.
    b) Second Class Delivery (70.88K): Significant, indicating a preference for cost savings.
    c) First Class Delivery (43.1K): Moderate, appealing to those valuing faster delivery.
    d) Same day Delivery (16.17K): Smallest, reflecting premium pricing and urgency.
  
 This represents that people mostly prefer Standard(free) delivery.  
  
  ### [3] Payment Mode
     a) Cash on Delivery (43%): Predominant choice, indicating a substantial portion of customers prefer paying upon receipt.
     b) Online Payments (35%): Growing trend, highlighting increasing acceptance of digital payment methods.
     c) Card Payments (22%): Smaller but significant, showing a preference for cashless transactions.

In conclusion, while cash on delivery remains popular, there's a notable shift towards online and card payments, emphasizing the importance of offering diverse payment options to cater to evolving customer preferences.
  
      
 ### [4] Some other insights
 
 ### Sales by Month
    The area chart spanning two years illustrates a notable trend: sales exhibit a steady increase as each year progresses towards its end. This pattern hints at a seasonal surge in purchasing behavior, indicating an opportunity for businesses to strategically plan promotions and inventory management to      maximize revenue during peak periods.
 

 ### Sales by Category and Segment
 
    a)Office Supplies Dominance: Office supplies lead in sales compared to tech gadgets and furniture, indicating a consistent demand for workplace essentials.
    b)Phone Sales Superiority: Within office supplies, phones emerge as the top-selling item, reflecting a strong consumer preference for mobile devices.
    c)Consumer Segment Preeminence: Among sales segments, the consumer segment stands out as the top performer, surpassing both home office and corporate segments. This suggests a significant market share and purchasing power among individual consumers.
         
### Sales by Region

    a)Regional Disparity: West leads with 33%, while South lags at 16%, indicating varying market performances.
    b)Growth Potential: South's lower sales suggest untapped opportunities for expansion or targeted marketing efforts.
    c)Strategic Allocation: With strong sales in West and East, focusing resources there could optimize market positions.

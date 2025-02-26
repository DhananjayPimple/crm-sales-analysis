## CRM Sales Data Analaysis Using Power BI

![Power BI](https://github.com/DhananjayPimple/crm-sales-analysis/blob/main/Dashboard.png?raw=true)

## 🚀 Live Dashboard Link - 
https://app.powerbi.com/view?r=eyJrIjoiODE3NjRkZDMtZmJkZC00M2E4LTk2NjAtZGEyYjgyMzAyMDY5IiwidCI6ImNlNWViZjI5LTA0NjktNDRjOS1hODhhLTJmNmYzNDQyMWU3OSJ9

## 📖 Project Overview

This project involves a detailed analysis of a Multinational IT Company's sales data collected from crm tools using Power BI. The goal is to gain valuable insights and answer various business questions faced by stakeholders based on the dataset. The following README provides a detailed information of the project's objectives, business problems, solutions, findings, and conclusions. The dataset includes information about open sales pipelines and closed sales deals across company's various locations globally.

## Objective 

- Use Power BI to analyze and visualize the CRM sales data to investigate the sales performance across regions, countries, and products.
- Visualize total sales, perhaps through a line chart or a bar chart, showing trends over time.
- A slicer or filter for selecting specific regions, countries, industries and services.
- Visualizations that show sales distribution across selected dimensions.
- A map visualization that displays sales geographically based on the selected filters

## Meta-Data

### 1. TCV (Total contract value)

Measures the total value of a customer contract, including one-time fees, service fees, and recurring charges. It's useful for assessing the health of a company's customer base. TCV is a more accurate projection of future revenue.


### 2. ACV (Anuual contract value)

Measures the average annual revenue a customer generates for a business. It's useful for assessing sales team performance and understanding revenue growth from new bookings. ACV is calculated by dividing the total contract value by the number of years in the contract.

### 3. Closed Deals

Refer to sales opportunities that have been successfully completed and finalized, meaning a customer has signed a contract and the sale is considered as "won".

### 4. Open Pipeline

Represents all the potential sales opportunities currently in progress at various stages of the sales process, meaning they haven't been closed yet and are still being actively pursued by the sales team.

### 5. Closed Won

A deal that was successfully closed and a prospect became a customer. This could be a new customer acquisition or upselling an existing customer.

### 6. Closed Lost

A deal that was pursued but did not result in a successful sale.

## Data Transformation Steps 

- Appended the two datasets named "Open Piplines" & "Closed Deals" into one inside the power query as they were smaller in size to 
  simplify the data transformation and analysis.
- Removed un-necessary columns from the datasets as they were irrelevent to the analysis and may occupy un-necessary space.
- After carefully examining the dataset it was found that the dataset was mostly clean except some data formatting issues which are 
  listed below
  
  1. AccountId >> Account Id in both datasets.
  2. As USA & United States both present in countries column >> USA replaced to United States.
  3. LiveLife(Mexico) & LiveLife(Mexico ) both present in Account Name Column >> LiveLife(Mexico ) to LiveLife(Mexico).
  4. Industry column was not present in closed_deals, hence in appended table it becomes empty in 69%. Used dax function to create new 
     industry column.
  5. Calculated TCV - ACV >> Using DAX Measures.
  6. Created YEAR column from Close Date.
  7. Created Calculated Column Stage 2 to slice values based on "Closed Deals" & "Open Pipeline".



## Business Problems & Solutions

### Which Country is the most profitable?

  Ans - Mexico.
  
  As we can see the below snapshot from the dashboard it is clear that "Mexico" has the highest percentage of Total Contract Value among all the countries.

  ![Country](https://github.com/DhananjayPimple/crm-sales-analysis/blob/main/Business%20Ans%20Snapshots/Country.png?raw=true)
  
### In sales, what is the difference between TCV and ACV?

  Ans - 548.4 Million Dollers

  As we can see the below snapshot from the dashboard it can be seen that the difference between the TCV & ACV is 548.4 Million Dollers.

  ![Difference](https://github.com/DhananjayPimple/crm-sales-analysis/blob/main/Business%20Ans%20Snapshots/Difference.png?raw=true)
  
### Which service has the highest Margin % for deals won?

  Ans - Business Solutions.

  Though all of the top three services "Business Solutions", "Cloud & Security" and "Tech Infrastructure Services" have performed very well but Business Solutions came out as top 
  performing service in terms of sales deals won securing 36.61% TCV Margin.

  ![Services](https://github.com/DhananjayPimple/crm-sales-analysis/blob/main/Business%20Ans%20Snapshots/Services.png?raw=true)

###	Which service has the lowest Margin % for deals in pipeline?

    Ans - Cloud & Security.

    From all the business services offered by the company, "Cloud & Security" have the lowest TCV margin percentage for sales in pipeline as 21.64%.

  ![Services2](https://github.com/DhananjayPimple/crm-sales-analysis/blob/main/Business%20Ans%20Snapshots/Services2.png?raw=true)
  
- Based on the insights provided in your report, what specific actions would you recommend to a seller to optimize their selling strategy? Please explain your reasoning.


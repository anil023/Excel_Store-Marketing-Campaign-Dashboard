# Store Marketing Campaign
## Define the Question
Data from a superstore marketing campaign is accessible on Kaggle [(link)](https://www.kaggle.com/datasets/ahsan81/superstore-marketing-campaign-dataset "Kaggle Link to the Dataset"). This repository documents the data analysis conducted on the provided dataset using Microsoft Excel. The primary objectives of this analysis include identifying the marketing campaign that will maximize sales profits for the store and pinpointing specific customer age groups for potential future customer acquisition projects.

The dataset served as the cornerstone for performing in-depth data analysis and generating a variety of insights using visualizations in Microsoft Excel. Additionally, it served as the source of inspiration for creating an Excel-based dashboard that captures the customer and sales demographics during the trial and for each campaign.

## Collecting Details:
- **dictionary.png** : describes the variables/column names present in the raw data file
  ![dictionary.png](https://github.com/anil023/Store-Marketing-Campaign/blob/bf3c72c976ca68970ed9146b3c0f720883c6c2be/dictionary.png "Link to the File")
- **[ifood_df.csv](https://github.com/anil023/Store-Marketing-Campaign/blob/bf3c72c976ca68970ed9146b3c0f720883c6c2be/ifood_df.csv "Link to the File")** : raw data file exported from Kaggle
- **[Store Marketing Campaign Analysis.xlsx](https://github.com/anil023/Store-Marketing-Campaign/blob/bf3c72c976ca68970ed9146b3c0f720883c6c2be/Store%20Marketing%20Campaign%20Dashboard.xlsx "Link to the File")** : excel encompassing all the data analysis and visualizations
     - sheet **"ifood_df"** is the original datset
     - sheet **"Worksheet"** is the clean dataset
     - sheets **"Plots"** and **"Plots_2"** contains numerous data visualization pivot tables and plots
     - sheets **"Dashboard"** contains the excel based dashboard for the data
- **[Store Marketing Campaign Analysis.pptx](https://github.com/anil023/Store-Marketing-Campaign/blob/bf3c72c976ca68970ed9146b3c0f720883c6c2be/Store%20Marketing%20Campaign%20Analysis.pptx "Link to the File")** : presentation deck from the data analysis

## Data Cleaning
- The raw dataset had 2206 row items, of which 184 were determined as **duplicates** and hence deleted to create the initial "Worksheet" sheet in the Excel.
- The **Age** numerical variable is converted into a categorical variable **Age Brackets**. Similarly we also built **Income Brackets**, **Last Purchase**, **Website Visits** and **Customer Loyalty**.
- The **Education Status** is a categorical variable that combines corresponding columns from the raw dataset. Similarly we also created **Marital Status**.
- Remaining variables are renamed to ease the understanding of the dataset.

## Data Analysis
- Campaign 6 has demonstrated its capability to maximize sales for the store.
  - Campaign: 6 achieved the **highest sales ($304.7k)** in the trial. It’s a substantial 30% increase over the next best-performing campaign.
  - The campaign ranks second to last in terms of average per customer sales($980/customer). It’s about 40% lower than the highest **average per customer sales** (from Campaign: 5).
  - One key factor contributing to Campaign: 6's higher total sales was its ability to capture approximately **15% of the customer base**. In contrast Campaign 5 and 1 both struggled with roughly 50% lower customer capture rates.
  - The customer base captured through the campaign had a very close resemblance to the trial base especially in the income bracket.
![image](https://github.com/anil023/Store-Marketing-Campaign/assets/19195341/0c3abdd4-c039-41b0-af5e-050f240e81f1 "Total Sales vs Campaign")

- Age group “20-29” is an ideal candidate for future customer acquisition campaigns.
  - Throughout each campaign, the average sales per customer within the “20-29” age group has consistently exceeded or matched the performance of other age groups.
  - Overall average sales confirm that the age group “20-29” has per customer sales worth $973, about 23% higher than the next best age group.
  - The age group also has the fewest number of customers. It’s nearly 64% lower than the next largest age group.
  - With robust customer loyalty among all age groups. Given the promising sales performance, targeting this age group is expected to yield continued sales growth in the coming years.
![image](https://github.com/anil023/Store-Marketing-Campaign/assets/19195341/6ef41591-e9bc-4870-9225-26b3c5013e56 "Averages Sales/customer and Number of Customers by Age")

- Excel Dashboard
  ![image](https://github.com/anil023/Store-Marketing-Campaign/assets/19195341/db86f8f2-63f5-4d71-9964-4b9fd45fca7f "Overall Trial Status")
  - TOTAL SALES AMOUNT PLOT: The trial's total sales amount is $1228.2k, primarily driven by wines, meat, and gold products across all age groups. Notably, about 75% of sales come from customers aged between 40-69.
  - SALES SOURCE PLOT: Across all age groups, the store and web emerged as the primary sales channels, while catalog and discounts contributed similarly across most age groups.
  - AVERAGE SALES PLOT: Average spending tends to be higher in the 20-29 age group, gradually decreasing until age 49. Beyond 50 years, customers appear to gradually increase their spending.

Following plots provide insights into customer demographics, facilitating comparisons during in-depth campaign analysis and helping identify any campaign biases towards specific customer segments.
  - NUMBER OF CUSTOMERS PLOT: In total, we have 2021 customers, with approximately 78% falling within the 40-69 age range. The number of customers in the 20-29 age group is notably low.
  - MARITAL STATUS PLOT: The majority (64%) of customers are couples, either married or living together.
  - INCOME BRACKET PLOT: Income bins were carefully selected to ensure an equal distribution of customers within each bin. This aids in identifying campaign biases and assessing the need to target every income bracket for maximum sales.
  - EDUCATION STATUS PLOT: A significant proportion of customers are well-educated, with approximately 50% holding graduate degrees.
  - LAST PURCHASE PLOT: Several customers have not made a purchase in over 2 months. These plots can help determine which campaign strategies might reactivate these customers and boost sales.
  - CUSTOMER LOYALTY PLOT:This plot highlights a substantial number of loyal customers, many of whom have been with us for 6-8 years. It also underscores the importance of new customer acquisition efforts to drive further sales growth.

For more in-depth Campaign analysis, use the dashboard and the provided Pivot Chart Slicer for each Campaign one at a time.

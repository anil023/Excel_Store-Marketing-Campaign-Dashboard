# Sales and Customer Analysis for a Store
## Define the Question
Data from a superstore(iFood) marketing campaign is accessible on Kaggle [(link)](https://www.kaggle.com/datasets/ahsan81/superstore-marketing-campaign-dataset "Kaggle Link to the Dataset"). This repository documents the data analysis conducted on this available dataset using Microsoft Excel. The primary objectives of this analysis include identifying customer groups for future customer acquisition campaigns that could help maximize sales.

The dataset served as the cornerstone for performing data analysis and generating a variety of insights using visualizations in Microsoft Excel. Additionally, it served as the source of inspiration for creating an Excel-based dashboard that captures the store, customer and sales demographics.  

![image](https://github.com/anil023/Store-Marketing-Campaign/assets/19195341/fd799934-c31d-4786-9047-853e7ea9c36f "Final Excel Dashboard")
<!--- ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- --->
<!--- ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- --->
## Collecting Details:
- **dictionary.png** : describes the variables/column names present in the raw data file
  ![dictionary.png](https://github.com/anil023/Sales-and-Customer-Analysis-for-a-Store/blob/b6edf445a8989a7bf821f568acdb719f918787f5/dictionary.png "Link to the File")
- **[ifood_df.csv](https://github.com/anil023/Sales-and-Customer-Analysis-for-a-Store/blob/b6edf445a8989a7bf821f568acdb719f918787f5/ifood_df.csv "Link to the File")** : raw data file exported from Kaggle
- **[Sales and Customer Analysis Dashboard.xlsx](https://github.com/anil023/Sales-and-Customer-Analysis-for-a-Store/blob/b6edf445a8989a7bf821f568acdb719f918787f5/Sales%20and%20Customer%20Analysis%20Dashboard.xlsx "Link to the File")** : excel encompassing all the data analysis and visualizations
     - sheet **"rawdata"** is the filtered and cleaned datset
     - sheet **"tables"** contains the tables used to link the sales products and channels
     - sheet **"Data Analysis"** contains tables used in visualizations etc
     - sheet **"Dashboard"** contains the excel based dashboard for the data
     - sheet **"Version Control"** contains the general instructins for the dashboard
<!--- ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- --->
<!--- ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- --->
## Data Cleaning
- The data stored as csv is imported using Power Query and cleaned using Power Query commands for correct data types.
- The final dataset comprises 2,205 row items. I did not remove any potential duplicates flagged by Excel since there are no distinguishing columns, such as customerID, to confirm they are duplicates. It is possible for distinct customers to exhibit similar purchase behaviors.
- The **Age** numerical variable is converted into a categorical variable **Age Bracket**. Similarly we also built **Income Bracket**, **Last Purchase**, **Website Visits** and **Customer Loyalty** variables from their corresponding numerical variables utilizing logical reasons to split the data that would make sense to read and analyze the data.
- The **Education Status** is a categorical variable that combines corresponding combination of columns from the raw dataset. Similarly we also created **Marital Status**.
- Remaining variables are renamed to ease the understanding of the dataset.
<!--- ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- --->
<!--- ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- --->
## Data Analysis
### Age-Based Sales of Products
<!--- Drop Down Menu --->
<details>
<summary><i>Understand the Section: "Age-Based Sales of Products" </i></summary>
<i>
<p align="center">
<img src="https://github.com/anil023/Store-Marketing-Campaign/assets/19195341/8c3ce306-c541-431d-bbd4-9bf4fb087b86" width="500">
</p>
  
When using the "Age-Based Sales of Products" section of the dashboard we need two inputs:
<li>Total Sales/Average Sales </li>
<li>Product(select only one product at a time) </li>
Examining the column plot for the total sales of Fish products, it becomes clear that the age segment with the highest sales (indicated in red) of fish products is 40-49, whereas the age group 20-29 records the lowest sales (in blue). The sales of fish products generated revenue of approximately $83.3k, accounting for roughly 6.2 percent of the total sales revenue from all the products in the store. The top three age segments that contributed the most to the sales of fish products are 40-49, 60-69, and 50-59.   
<!--- 83.3/1338 = 0.0623--->
Observing the column plot for the average sales of Fish products, it is worth noting that the age segment 20-29 spent the most on fish products on average, whereas the age group 40-49 spent the least. The top three age groups with the highest average spending on fish products are 20-29, 70 and Older, and 60-69.
</i>
</details>

Based on the preliminary analysis of the section 'Age-Based Sales of Products', several key insights can be derived as follows:

From Total Sales:
- Wine, Meat, and Gold products sales revenue collectively constituted approximately 85% of the store's total sales revenue, with wine sales accounting for about half of the total sales revenue from the store.
<!--- 675.1+364.5+97.1/1338=0.849 --->
- The age groups encompassing customers aged 40-69 collectively accounted for approximately 75% of the store's total sales revenue, with the 40-49 age group emerging as the major customer segment across all product categories, except for Wine.
<!--- 347.4+335.7+326/1338=0.754--->
- Remarkably, the age group 20-29 consistently had the lowest sales revenue across all product categories.

From Average Sales:
- The customers within age group 20-29 and who are aged 60 and older, tend to spend the most across various product categories at the store.
<!--- 927>823>689--->
- Conversely, the 40-49 age group had the least average spending for most of the product categories, except for Wine, where the 30-39 age group spent the least.
<!---248>237--->
- In the case of Gold products, the age group 50-59 replaces the 70 and Older group among the top three customer segments with maximum average sales.
<!--- 47>43--->
- Comparing age groups, it's evident that customers in the age group 20-29 spent the most, about 55% more than the aggregate age group 40-69, and approximately 85% more than the age group 40-49.
<!--- 927>(347.4+335.7+326)/(691+528+473)=596>503--->
- Notably, the 70 and Older and 60-69 age groups consistently emerge as the consecutive next-best age groups with the highest average spending across product categories.
<!--- 927>823>689--->

Considering the insights from the Total Sales we woud have recommended to target the age group 40-69, but it appears that the age group 20-29 shows promising potential for future sales growth due to their high average spending. Additionally, the 70 and Older and 60-69 age groups also offer strong opportunities for targeting, as they consistently exhibit above-average spending habits.

<!--- HTML Table--->
<table>
    <thead>
        <tr>
            <th rowspan=2>AGE BRACKETS</th>
            <th colspan=7>TOTAL SALES(in $1000)</th>
            <th colspan=7>AVERAGE SALES(IN $)</th>
        </tr>
        <tr>
            <th>FISH</th>
            <th>FRUITS</th>
            <th>GOLD</th>
            <th>MEAT</th>
            <th>SWEET</th>
            <th>WINE</th>
            <th>AGGREGATE TOTALS by age</th>
            <th>FISH</th>
            <th>FRUITS</th>
            <th>GOLD</th>
            <th>MEAT</th>
            <th>SWEET</th>
            <th>WINE</th>
            <th>AGGREGATE AVERAGES by age</th>
        </tr>
    </thead>
    <tbody>
        <tr>
          <td>20-29</td>
          <td>2.7</td>
          <td>1.7</td>
          <td>2.9</td>
          <td>13.9</td>
          <td>1.8</td>
          <td>16.9</td>
          <td>39.9</td>
          <td>63</td>
          <td>40</td>
          <td>67</td>
          <td>324</td>
          <td>42</td>
          <td>393</td>
          <td>927</td>
        </tr>
      <tr>
          <td>30-39</td>
          <td>12.7</td>
          <td>9.1</td>
          <td>13.3</td>
          <td>55.2</td>
          <td>8.9</td>
          <td>79.6</td>
          <td>178.7</td>
          <td>38</td>
          <td>27</td>
          <td>40</td>
          <td>164</td>
          <td>26</td>
          <td>237</td>
          <td>532</td>
        </tr>
      <tr>
          <td>40-49</td>
          <td>22.3</td>
          <td>15.7</td>
          <td>26.6</td>
          <td>94</td>
          <td>17.3</td>
          <td>171.4</td>
          <td>347.4</td>
          <td>32</td>
          <td>23</td>
          <td>38</td>
          <td>136</td>
          <td>25</td>
          <td>248</td>
          <td>503</td>
        </tr>
        <tr>
          <td>50-59</td>
          <td>19.1</td>
          <td>14.4</td>
          <td>24.8</td>
          <td>85.3</td>
          <td>13.7</td>
          <td>178.4</td>
          <td>335.7</td>
          <td>36</td>
          <td>27</td>
          <td>47</td>
          <td>162</td>
          <td>26</td>
          <td>338</td>
          <td>636</td>
        </tr>
      <tr>  
          <td>60-69</td>
          <td>20.1</td>
          <td>13</td>
          <td>23.9</td>
          <td>86.3</td>
          <td>13.8</td>
          <td>168.9</td>
          <td>326</td>
          <td>42</td>
          <td>28</td>
          <td>51</td>
          <td>182</td>
          <td>29</td>
          <td>357</td>
          <td>689</td>
        </tr>
      <tr> 
          <td>70 and Older</td>
          <td>6.4</td>
          <td>4.2</td>
          <td>5.8</td>
          <td>29.8</td>
          <td>4.4</td>
          <td>59.8</td>
          <td>110.3</td>
          <td>48</td>
          <td>31</td>
          <td>43</td>
          <td>222</td>
          <td>33</td>
          <td>446</td>
          <td>823</td>
        </tr>
      <tr> 
          <th>AGGREGATE TOTALS by products</th>
          <td>83.3</td>
          <td>58.2</td>
          <td>97.1</td>
          <td>364.5</td>
          <td>59.8</td>
          <td>675.1</td>
          <th>AGGREGATE AVERAGE by products</th>
          <td>38</td>
          <td>26</td>
          <td>44</td>
          <td>165</td>
          <td>27</td>
          <td>306</td>
          <td></td>
        </tr>
    </tbody>
</table>

<!---  BACKUP TABLE
| AGE BRACKET | TOTAL SALES | AVERAGE SALES |

20 2.7/1.7/2.9/13.9/1.8/16.9=39.9                   63/40/67/324/42/393=927                  WMGFSR   211
30 12.7/9.1/13.3/55.2/8.9/79.6=178.7                38/27/40/164/26/237=532                  WMGFRS   
40 22.3/15.7/26.6/94/17.3/171.4=347.4               32/23/38/136/25/248=503                  WMGFSR   
50 19.1/14.4/24.8/85.3/13.7/178.4=335.7             36/27/47/162/26/338=636                  WMGFRS   3
60 20.1/13/23.9/86.3/13.8/168.9=326                 42/28/51/182/29/357=689                  WMGFSR   332
70 6.4/4.2/5.8/29.8/4.4/59.8=110.3                  48/31/43/222/33/446=823                  WMFGSR   12
Total 83.3/58.2/97.1/364.5/59.8/675.1               38/26/44/165/27/306
--->
<!--- ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- --->
<!--- ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- --->
### Age-Based Sales Channel Utilization
<!--- Drop Down Menu --->  
<details>
  <summary><i>Understand the Section: "Age-Based Sales Channel Utilization" </i></summary>
<i>
<p align="center">
  <img src="https://github.com/anil023/Store-Marketing-Campaign/assets/19195341/2dfa70ef-df00-43a6-9f06-dc12b3de4c57" width="500">
</p>
When using the "Age-Based Sales Channel Utilization" section of the dashboard we need two inputs:
<li>Total Sales/Average Sales </li>
<li>Channel(select only one channel at a time) </li>
Examining the column plot for the total sales through Catalog channel, we observe that the age segment of 60-69 emerges as the most frequent users (indicated in red) of catalogs. In contrast, the age group 20-29 displays the least inclination (in blue) towards utilizing catalogs. One particularly striking observation is the remarkable disparity in usage between the 60-69 age segment and the 20-29 group, with the former utilizing Catalogs approximately 725% more frequently.   
<!--- (1518-184)/184 = 7.25--->
When examining the average sales through catalogs, it's worth noting that the most enthusiastic age group to use catalogs is 20-29, while the age group 30-39 used them the least. The disparity in engagement is approximately 102% of group 30-39.
<!--- (4.3-2.1)/2.1--->
</i>
</details>

The analysis of sales channel utilization, based on age groups, unveils intriguing insights into customer behavior as below:
- It's worth noting that the majority of age groups show a preference for the in-store channel, followed by the web, catalogs, and deals channels, in that sequence. However, there are exceptions. The age group 20-29 appears to prioritize catalogs over the web, while the age group 40-49 leans towards deals over catalogs.
- A substantial portion of the total number of sales, approximately 67%, is attributed to sales through physical stores and the web, with brick-and-mortar stores contributing to around 39% of the total sales.
<!--- (12841+9042)/32828=0.6667 & 12841/32828=0.39--->
- Considering the overall utilization of these sales channels, age groups ranging from 40 to 69 demonstrate significant engagement, utilizing these mediums approximately 78% of the time. Among them, the age group 40-49 emerges as the most versatile in channel utilization.
<!---(9628+8230+7800)/32828=0.782--->
- Interestingly, the age group 20-29 consistently exhibits the lowest utilization across all sales mediums.
- On comparing the average number of sales, most age groups display relatively similar usage patterns across each sales medium. Nevertheless, there are notable exceptions.
- Age groups with customers aged 60 and older and 20-29 tend to have the highest usage across multiple mediums, indicating their receptiveness to a variety of sales channels.
<!---17.3>16.6>15.7--->
- Conversely, the age group 30-39 emerges as the lowest consumer of each sales medium, potentially reflecting a need for tailored marketing approaches to enhance their engagement.
- Of particular significance is the age group 70 and older, which not only utilized approximately 38% more channels than the age group 30-39 but also demonstrated around 15% higher usage than the combined 40-69 age group. 
<!---17.3-12.5/12.5=0.384 & 17.3 > (9628+8230+7800)/(691+528+473)=15.16 --->

In light of this analysis, the age group 70 and older clearly emerges as the most engaged and responsive to various sales channels, particularly the in-store and web channels. Therefore, for future sales growth, it is recommended to focus on strategies that further enhance the engagement of this age group through in-store and web channels. Additionally, a targeted approach to re-engage the age groups 60-69 and 20-29, with a particular emphasis on catalogs for the 20-29 group and deals for the 60-69 age group, may also prove beneficial.

|AGE BRACKETS|TOTAL:CATALOG|TOTAL:DEALS|TOTAL:STORE|TOTAL:WEB|AGGREGATE TOTAL BY AGE|AVERAGE:CATALOG|AVERAGE:DEALS|AVERAGE:STORE|AVERAGE:WEB|AGGREGATE AVERAGE BY AGE|
| ------------- |:-------------:| :-------------:|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|
|20-29| 184|66|267|157|674|4.3|1.5|6.2|3.7|15.7|
|30-39| 711|588|1743|1131|4173|2.1|1.8|5.2|3.4|12.5|
|40-49| 1510|1717|3740|2661|9628|2.2|2.5|5.4|3.9|14|
|50-59| 1414|1321|3171|2324|8230|2.7|2.5|6.0|4.4|15.6|
|60-69| 1518|1161|3011|2110|7800|3.2|2.5|6.4|4.5|16.6|
|70 and Older| 496|259|909|659|2323|3.7|1.9|6.8|4.9|17.3|
|**AGGREGATE TOTAL by channels**| 5833|5112|12841|9042|**AGGREGATE AVERAGE by channels**|18.2|12.7|36|24.8|

<!---BACKUP TABLE
20 184/66/267/157=674                   4.3/1.5/6.2/3.7=15.7                  SCWD
30 711/588/1743/1131=4173               2.1/1.8/5.2/3.4=12.5                  SWCD
40 1510/1717/3740/2661=9628             2.2/2.5/5.4/3.9=14                    SWDC
50 1414/1321/3171/2324=8230             2.7/2.5/6.0/4.4=15.6                  SWCD
60 1518/1161/3011/2110=7800             3.2/2.5/6.4/4.5=16.6                  SWCD
70 496/259/909/659=2323                 3.7/1.9/6.8/4.9=17.3                  SWCD
TOTAL 5833/5112/12841/9042/32828        18.2/12.7/36/24.8
--->
<!--- ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- --->
<!--- ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- --->
### STORE KPI's
- AGE:
<details>
<summary align="center"><i>Store KPI: Age of Customers</i></summary>
<p align="center">
<img src="https://github.com/anil023/Store-Marketing-Campaign/assets/19195341/c2ee7c0a-cbb4-4468-b855-cbe3e17fbb8e" width="500">
</p>
</details>

  We can observe a visually normal distribution of customers among the age segments, with a notable number of customers in each category. It's worth noting that the age group 20-29 is represented by 43 records, while the age group 70 and older is represented by 134 records; these are relatively smaller sample sizes, and hence their rankings might be less reliable due to the potential for greater variability in the estimates.  

  To gain a deeper understanding of whether the mean values differ significantly, particularly for the age groups with smaller sample sizes, it would be beneficial to employ ANOVA tests. Additionally, I would recommend the inclusion of more customers from these age groups in the study to enhance our confidence in comparing the averages of different age brackets. For this study we will accept the sample size as sufficient enough to instill confidence on the mean value comparisons performed above.  
- CUSTOMER COMPLAIN:
<details>
<summary align="center"><i>Store KPI: Customer Complain</i></summary>
<p align="center">
<img src="https://github.com/anil023/Store-Marketing-Campaign/assets/19195341/2ec166dd-4584-4add-bab2-b96bc6d05009" width="500">
</p>
</details>

  A very low percentage, less than 2% of customers in each age segment, have raised complaints. However, it is noteworthy that there is an unusually low number of complaints in the 50-59 age group, with only 1 complaint out of 527 customers. Conversely, the 60-69 age group has a higher number of complaints, with 7 out of 466 customers. This distribution is unusual as it deviates from a normal distribution curve and begs the question if there was a reason for this high/low numbers.
- NUMBER OF WEBSITE VISITS: 
<details>
<summary align="center"><i>Store KPI: Number of Website Visits</i></summary>
<p align="center">
<img src="https://github.com/anil023/Store-Marketing-Campaign/assets/19195341/e9f70da7-77a8-4819-8cd3-a034c2f0df5c" width="500">
</p>
</details>

  In total, about 56% of customers visit the website 5-10 times a month, while approximately 42% use it less than 5 times a month. We don't observe any huge discripancies in the distribution of the website users within different age groups but there is definitely more opportunities to increase the website usage more than 10 times a month through different campaigns. 
- CUSTOMER LOYALTY PERIOD:
<details>
<summary align="center"><i>Store KPI: Customer Loyalty Period</i></summary>
<p align="center">
<img src="https://github.com/anil023/Store-Marketing-Campaign/assets/19195341/78587e2f-f613-4897-9c1e-d80a4d1adb9f" width="500">
</p>
</details>

  Approximately 53% of customers have shown remarkable loyalty by staying with us for about 6-7 years. But we should also note that only a small percentage, around 3%, have been customers for a period ranging from 4-6 years. This data underscores the presence of a highly loyal customer base overall. Yet, there remains an opportunity for growth through targeted customer acquisition campaigns, particularly among age brackets such as 20-29, which can contribute to sales growth.  
- LAST PURCHASE: 
<details>
<summary align="center"><i>Store KPI: Last Purchase</i></summary>
<p align="center">
<img src="https://github.com/anil023/Store-Marketing-Campaign/assets/19195341/a2bafd1d-48a0-4ea9-97e8-59c849f72f55" width="500">
</p>
</details>

  A significant portion, about 67% of customers, haven't made a purchase from the store in more than 1 month, with a substantial segment (37%) indicating that their last purchase was more than 2 months ago. This trend suggests a potential opportunity for re-engagement and marketing strategies to bring back these customers through various sales channels.
<!--- ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- --->
<!--- ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- --->
### CUSTOMER DEMOGRAPHICS
- INCOME:
  <details>
  <summary align="center"><i>Customer Demographics: Income</i></summary>
  <p align="center">
  <img src="https://github.com/anil023/Store-Marketing-Campaign/assets/19195341/d4e5f46c-e33b-43cf-b725-901f83776484" width="500">
  </p>
  </details>

We observe a substantial increase in the percentage of low-income customers within the 30-39 age group compared to adjacent age groups. This is followed by a gradual decrease in the proportion of low-income customers as we move towards the "70 and Older" age group. This variation may contribute to the lower average sales observed within the 30-39 age group. In contrast, both mid-income and high-income customers demonstrate an opposing trend, transitioning from the 30-39 age group to the "70 and Older" group.

The 20-29 age group stands out with the highest proportion of high-income customers, which could explain the higher per-customer sales within this age group. Notably, the income distribution among the age groups can be summarized as 36% low income, 28% mid-income, and 36% high income.  
<!--- 35-12-53/62-10-28/47-29-24/32-38-30/25-39-36/16-39-45 = 36-28-36 --->
- MARITAL STATUS:
  <details>
  <summary align="center"><i>Customer Demographics: Marital Status</i></summary>
  <p align="center">
  <img src="https://github.com/anil023/Store-Marketing-Campaign/assets/19195341/7e65d6bc-f5c3-4d39-96b2-17cfe9f6e5d3" width="500">
  </p>
  </details>
  
The distribution of marital status across age groups reveals varying percentages. Majorly, about 35% of our customers are married, 27% are single, and 26% are in relationships or living together.  We can visually confirm that the proportion of married customers increases within the 20-49 age groups, then remains relatively stable at around 35% until the 70 and older age group.

Similarly, the 20-29 age group had the highest percentage of single customers, approximately 60%, which gradually declined as we progressed through the age brackets. The percentage of customers in relationships or living together has remained relatively constant, with a slight increase noted in the 60-69 age group. The number of customers who are widowed or divorced increases as we progress through the age groups, with a notable decrease in divorced customers after the age of 60.

It's important to note that the current analysis does not establish a clear correlation between marital status and sales. A more in-depth analysis is required to confirm any hypotheses regarding this relationship.
<!---60-31-20-21-18-11/0-4-11-14-12-8/19-42-44-36-35-34/21-24-24-24-30-31/0-0-2-4-5-15--->

- EDUCATION:
  <details>
  <summary align="center"><i>Customer Demographics: Education</i></summary>
  <p align="center">
  <img src="https://github.com/anil023/Store-Marketing-Campaign/assets/19195341/7303a947-86d4-4b48-85b0-ba6037523c93" width="500">
  </p>
  </details>
  
A significant 87% of customers hold a bachelor's degree or higher, with 49% of them having a bachelor's degree. The remaining customers have attained either master's or PhD degrees. As age progresses, we observe a declining percentage of customers with "2n Cycle," "Basic," and "Graduation" degrees, with the exception of a slight increase in both "2n Cycle" and "Graduation" degree holders within the 60-69 age group. Notably, customers with "Masters" and "PhD" degrees show a consistent upward trend across age brackets, although there is a minor dip in the proportion of "PhD" holders in the 60-69 age group, followed by a significant surge in the "70 and Older" age group.

We don't observe any correlation from our analysis between the education status and average sales at the store and would need further analysis to prove any relationship.
- KIDS:
  <details>
  <summary align="center"><i>Customer Demographics: Kids</i></summary>
  <p align="center">
  <img src="https://github.com/anil023/Store-Marketing-Campaign/assets/19195341/44fa4653-8700-4c68-94ba-b181dce2c8c4" width="500">
  </p>
  </details>
   
Approximately 66% of customers are without kids, while 33% have one kid. Interestingly, there is a conspicuous absence of customers with two kids in the 20-29 age group, and this pattern of a very low proportion, roughly 2%, holds true among other age groups as well. In the case of customers with one kid, there is a substantial surge between the 20-29 and 30-39 age groups, followed by a gradual decrease as we progress towards the "70 and Older" customer category. 

It's worth noting that the percentage of customers with no children is remarkably similar in the "20-29" and "70 and Older" age groups, prompting the hypothesis that the number of children in a family may impact sales. This observation gains significance, especially considering that 50% of the products sold are wine, followed by meat and gold products, none of which cater to children.

- TEENS:
  <details>
  <summary align="center"><i>Customer Demographics: Teens</i></summary>
  <p align="center">
  <img src="https://github.com/anil023/Store-Marketing-Campaign/assets/19195341/e6e8c2e4-aa0f-46ab-a93d-710340b00f38" width="500">
  </p>
  </details>
  
  
Around 62% of customers do not have teenagers in their households, while 36% have one teenager. It makes sense when the "20-29" age group is characterized by the absence of any teenagers. Similarly, customers aged 20-39 do not typically have two teenagers in their families. However, this changes gradually starting from the "30-39" age group, and the percentage of customers with two teens remains relatively constant at 4% for customers older than 50. Proportion of customers with one teenager experience an increasing trend as we progress through the age brackets, with a significant 140% surge occurring in the "40-49" age group, followed by a 38% decline in the "70 and Older" age group.

We don't notice any observable correlation between count of teenagers and sales provided by the customers.

<!--- ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- --->
<!--- ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- --->
## SUMMARY
To recommend an age group for future sales growth based on the above analyses, we should consider multiple factors such as average spending, sample size, and the distribution of income, number of kids within each age group. Additionally, the analysis should align with the company's strategic goals. Here's my recommendation:

**Age Group 20-29:**

**Statistical Reasons:**
1. **Average Spending:** The age group 20-29 exhibits the highest sum of averages for spending across various product categories, indicating the potential for higher sales within this age group.
2. **Income Diversity:** This age group shows a diverse distribution of income levels, with a significant percentage of high-income customers. This diversity can be leveraged for sales growth strategies catering to different income segments.
3. **No Teens and Few Kids:** With a lower percentage of customers with kids or teens, marketing efforts might be more focused on individual or couple-based purchases.
4. **Sample Size:** While the sample size for this age group is relatively small, the potential for sales growth based on average spending and income diversity makes it a compelling target.
5. **Education:** The majority of customers in this age group have at least a bachelor's degree, indicating a level of education that may make them receptive to targeted marketing and higher-end products.

It's important to note that the choice of an age group should align with the company's products, services, and marketing strategies. The age group recommendation is based on statistical insights, but other factors such as product appeal, competition, and market trends should also be considered in the decision-making process.

---

THANKS  
Anil Raju  
[LinkedIn](https://www.linkedin.com/in/rajuanil/)



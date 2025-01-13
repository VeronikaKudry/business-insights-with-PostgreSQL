# Northwind’s Sales Data Analysis
Compiled by: Veronika Kudriavtseva
## Project background
I am a Data Analyst at Northwind Traders, an international gourmet food distributor. Management is looking for insights to make strategic decisions in several aspects of the business. The projects focus on:
* Evaluating employee performance to boost productivity,
* Understanding product sales and category performance to optimize inventory and marketing strategies,
* Analyzing sales growth to identify trends, monitor company progress, and make more accurate forecasts,
* Evaluating customer purchase behavior to target high-value customers with promotional incentives.

### Data used
This project fetches and analyzes the data from a rich [Northwind database](https://github.com/pthom/northwind_psql/tree/master). The following part of the database is used for the project: 

![image](https://github.com/user-attachments/assets/4e2755a8-0b1e-485d-8853-513e706c8182)

## Summary of Insights
### Employee Sales Performance
For the analysed period, the top-selling employee is **Margaret Peacock** with total sales of about \$250,000, ranking 1st with 156 orders and contributing 18% to total sales. **Janet Leverling** follows closely as the second top-seller, achieving around \$213,000 in total sales, with 127 orders and a 16% sales contribution. 
On the other end, **Steven Buchanan** is the lowest-selling employee with approximately \$76,000 in total sales, completing 42 orders and contributing 6% to overall sales. Close to him are **Michael Suyama** and **Anne Dodsworth**, with sales of around \$78,000 and \$83,000 respectively, both contributing 6% to the total sales.
<p align="center">
 <img src="https://github.com/user-attachments/assets/fc6b8d18-8713-43c8-8601-af353e987bf6"/>
</p>
By analysing the granular data, I can highlight Janet Leverling’s exceptional performance, achieving the highest quarterly sales of approximately $68,000. It may also be valuable to explore the underlying factors behind this result to identify potential insights that could benefit other employees.
<p align="center">
    <img src="https://github.com/user-attachments/assets/e6d187c6-6b16-4e1d-b132-ed6c831d9d30"/>
</p>

### Product Sales and Category Performance
For the analysed period we see the overall upward trend of monthly sales running total with slightly steeper increase in Dec'97-Apr'98.
<p align="center">
 <img src="https://github.com/user-attachments/assets/12abc6ee-67da-432b-90b0-4e93095b6dbe"/>
</p>

There are no noticeable trends in the Month-Over-Month Sales Change Rate. However with additional data (such as information about any marketing campaigns) it still can be valuable.
<p align="center">
 <img src="https://github.com/user-attachments/assets/ea2be1ca-306c-4db6-90da-193cb0038346"/>
</p>

When data is segmented by categories, the top-performing category is Beverages, with sales totalling about $ 268,000, accounting for 21% of the overall sales. The top two categories, Beverages and Dairy Products, dominate sales, together contributing 40% of the total. The remaining six categories collectively contribute 60%, with more even distribution among them.
<p align="center">
 <img src="https://github.com/user-attachments/assets/7035dcb8-646b-446d-9ff7-c7486d7672a3"/>
</p>

Drilling down further into each category helps to identify top products for each category. It is important to keep these products in stock and market them prominently.
<p align="center">
 <img src="https://github.com/user-attachments/assets/2af55d04-d21a-4641-931f-9b998b1f5183"/>
</p>

### High-Value Customers 
The analysis identified 64 customers with above-average order values from the 91 unique customers. Among them, three companies stand out: QUICK-Stop, Ernst Handel, and Save-a-lot Markets, each placing over 20 orders and reaching impressive total spending exceeding $100,000—$104,861, $101,717, and $100,041, respectively. The remaining companies exhibit much lower order volumes and spending. The full list (sorted in descending order by total spending) is provided in the ["*Strategic Business Insights with PostgreSQL.ipynb*"]( https://github.com/VeronikaKudry/business-insights-with-PostgreSQL/blob/2f2714d4416e250b5269430b8f932ef64836ff47/Strategic%20Business%20Insights%20with%20PostgreSQL.ipynb) notebook.

## Technical Details
The analysis leverages:
* PostgreSQL (window functions, aggregate functions, common table expressions and ranking functions) for data querying, 
* Python libraries like pandas for data manipulation,
* matplotlib and seaborn for visualization.  

You can find the entire project with the code in the ["*Strategic Business Insights with PostgreSQL.ipynb*"]( https://github.com/VeronikaKudry/business-insights-with-PostgreSQL/blob/2f2714d4416e250b5269430b8f932ef64836ff47/Strategic%20Business%20Insights%20with%20PostgreSQL.ipynb) notebook.

### To run the notebook on your machine:
1. you must have PostgreSQL installed and connected to your local Northwind database. You can find below the detailed guides to help you with this setup process:
    * [Windows](https://www.dataquest.io/blog/install-postgresql-14-7-on-windows-10/?_gl=1*1ww7b99*_gcl_au*MjEyMjk1MzI0Ny4xNzM0ODY5OTE1*_ga*MTYyNjA4OTkzNC4xNzM0ODY5OTE0*_ga_YXMFSKC6DP*MTczNjcxMzQxMC4xNS4xLjE3MzY3MTM1NDIuNS4wLjEwODAxNzE0NDA.)
    * [MacOS](https://www.dataquest.io/blog/install-postgresql-14-7-for-macos/?_gl=1*1j4kgyq*_gcl_au*MjEyMjk1MzI0Ny4xNzM0ODY5OTE1*_ga*MTYyNjA4OTkzNC4xNzM0ODY5OTE0*_ga_YXMFSKC6DP*MTczNjcxMzQxMC4xNS4xLjE3MzY3MTM1NzguNjAuMC4xMDgwMTcxNDQw)
    * [Ubuntu](https://www.dataquest.io/blog/install-postgresql-14-7-on-your-ubuntu-system/?_gl=1*1j4kgyq*_gcl_au*MjEyMjk1MzI0Ny4xNzM0ODY5OTE1*_ga*MTYyNjA4OTkzNC4xNzM0ODY5OTE0*_ga_YXMFSKC6DP*MTczNjcxMzQxMC4xNS4xLjE3MzY3MTM1NzguNjAuMC4xMDgwMTcxNDQw)
2. you must create the credentials file - "*Credentials52.json*" with your password to access the database on your device: 
{
    "username": "postgres",
    "password": "yourpasswordhere"
}
3. you must have required libraries installed, which are listed in "*requirements.txt*". 

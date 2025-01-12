# Strategic Business Insights with PostgreSQL

This project fetches and analyzes the data from a rich [Northwind database](https://github.com/pthom/northwind_psql/tree/master), which provides a real-world-like platform for exploring and analyzing sales data of an international gourmet food distributor. The goal of the project is to provide actionable insights for strategic decision-making. Key focus areas include:
* evaluating employee performance,
* optimizing product sales and inventory strategies,
* identifying sales growth trends for accurate forecasting,
* understanding customer behavior to target high-value customers with promotions. 

The analysis leverages:
* PostgreSQL (window functions, aggregate functions, common table expressions and ranking functions) for data querying, 
* Python libraries like pandas for data manipulation,
* matplotlib and seaborn for visualization.

You can find the code and visuals in the "*Strategic Business Insights with PostgreSQL.ipynb*" notebook above. 

## To run the notebook on your machine:
1. you must have PostgreSQL installed and connected to your local Northwind database. You can find below the detailed guides to help you with this setup process:
*[Windows](https://www.dataquest.io/blog/install-postgresql-14-7-on-windows-10/?_gl=1*1ww7b99*_gcl_au*MjEyMjk1MzI0Ny4xNzM0ODY5OTE1*_ga*MTYyNjA4OTkzNC4xNzM0ODY5OTE0*_ga_YXMFSKC6DP*MTczNjcxMzQxMC4xNS4xLjE3MzY3MTM1NDIuNS4wLjEwODAxNzE0NDA.)
*[MacOS](https://www.dataquest.io/blog/install-postgresql-14-7-for-macos/?_gl=1*1j4kgyq*_gcl_au*MjEyMjk1MzI0Ny4xNzM0ODY5OTE1*_ga*MTYyNjA4OTkzNC4xNzM0ODY5OTE0*_ga_YXMFSKC6DP*MTczNjcxMzQxMC4xNS4xLjE3MzY3MTM1NzguNjAuMC4xMDgwMTcxNDQw)
*[Ubuntu](https://www.dataquest.io/blog/install-postgresql-14-7-on-your-ubuntu-system/?_gl=1*1j4kgyq*_gcl_au*MjEyMjk1MzI0Ny4xNzM0ODY5OTE1*_ga*MTYyNjA4OTkzNC4xNzM0ODY5OTE0*_ga_YXMFSKC6DP*MTczNjcxMzQxMC4xNS4xLjE3MzY3MTM1NzguNjAuMC4xMDgwMTcxNDQw)
2. you must create the credentials file - "*Credentials52.json*" with your password to access the database on your device: 
{
    "username": "postgres",
    "password": "yourpasswordhere"
}
3. you must have required libraries installed, which are listed in "*requirements.txt*". 

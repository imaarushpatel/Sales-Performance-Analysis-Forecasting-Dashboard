# Sales-Performance-Analysis-Forecasting-Dashboard
This project focuses on analyzing and forecasting sales performance using a real-world retail dataset. The process involves data cleaning, exploratory analysis, time-series forecasting, and dashboard creation using Power BI for business insights.


🗂 Dataset
Source: Superstore Dataset (Kaggle)

Format: CSV

Key Fields: Order Date, Sales, Profit, Region, Category, Sub-Category

Data Cleaning (Python)
Performed using pandas:

Removed irrelevant columns (Customer Name, Product ID, etc.)

Converted Order Date to datetime

Created new fields like Month and Profit Margin

python
df['Order Date'] = pd.to_datetime(df['Order Date'], infer_datetime_format=True, errors='coerce')
df['Month'] = df['Order Date'].dt.to_period('M')
df['Profit Margin'] = df['Profit'] / df['Sales']
Exploratory Data Analysis (EDA)
Visualizations were generated using Matplotlib and Seaborn:

Sales by Region: Bar chart

Monthly Sales Trend: Line chart

Profit by Category: Boxplot

Forecasting Sales (Python - Linear Regression)
Built a simple time-series forecasting model using scikit-learn:

Converted monthly sales into numerical features

Trained and tested using a train-test split

Plotted actual vs predicted sales for visual comparison

python
model = LinearRegression()
model.fit(X_train, y_train)
y_pred = model.predict(X_test)

Power BI Dashboard
Final visuals presented in Power BI:

KPI Cards: Total Sales, Total Profit, Profit Margin

Line Chart: Monthly sales trend with forecast

Bar Chart: Regional sales performance

Pie Chart: Category-wise distribution

Interactive filters: Region, Category, Time Period

<!-- Replace with actual path -->

Key Takeaways
Automated data cleaning and transformation using Python

Used linear regression for basic sales forecasting

Built a fully interactive dashboard in Power BI

Enabled insights into top-performing regions and categories

How to Run
Clone this repo

Open Sales_Analysis.ipynb in Jupyter Notebook or VS Code

Download and place SampleSuperstore.csv in the same directory

Run each cell step-by-step

Open Power BI and load CleanedSuperstore.csv for visualization

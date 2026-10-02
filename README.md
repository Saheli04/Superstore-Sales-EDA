
# 📊 Superstore Sales — Exploratory Data Analysis

A comprehensive **Exploratory Data Analysis (EDA)** project on the Global Superstore dataset using Python, Pandas, NumPy, Matplotlib, and Seaborn.

The project analyzes **51,290 sales transactions** across products, customers, categories, markets, regions, discounts, shipping, sales, and profitability to identify meaningful business patterns and insights.


## 📌 Project Overview

The objective of this project is to perform a complete exploratory analysis of Superstore sales data and transform raw transactional data into meaningful business insights.

The analysis covers:

- Data inspection and quality analysis
- Missing-value analysis
- Duplicate detection
- Date-time feature engineering
- Statistical analysis
- Sales and profit analysis
- Category and sub-category performance
- Market and regional analysis
- Customer segment analysis
- Product performance
- Customer analysis
- Discount and profitability analysis
- Shipping analysis
- Correlation analysis
- Yearly, quarterly, and monthly sales trends
- Business KPI analysis

The complete analysis was performed in **Google Colab using Python**.

---

## 🎯 Project Objectives

The main objectives of this project are to:

- Understand the structure and characteristics of the dataset
- Assess data quality and missing values
- Detect duplicate records
- Perform data preprocessing
- Engineer useful date and shipping features
- Analyze sales and profitability
- Identify high-performing categories and sub-categories
- Compare market and regional performance
- Analyze customer segments
- Identify top-performing and loss-making products
- Study the relationship between sales, profit, and discounts
- Analyze shipping modes and shipping duration
- Explore correlations between numerical variables
- Identify important business patterns and trends

---

## 📂 Dataset

The original dataset contains:

- **51,290 rows**
- **24 columns**

After feature engineering, the analysis dataframe contains **29 columns**.

### Dataset Features

| Feature | Description |
|---|---|
| Row ID | Unique row identifier |
| Order ID | Unique order identifier |
| Order Date | Date when the order was placed |
| Ship Date | Date when the order was shipped |
| Ship Mode | Shipping method |
| Customer ID | Unique customer identifier |
| Customer Name | Customer name |
| Segment | Customer segment |
| City | Customer city |
| State | Customer state |
| Country | Customer country |
| Postal Code | Postal code |
| Market | Market |
| Region | Geographic region |
| Product ID | Unique product identifier |
| Category | Product category |
| Sub-Category | Product sub-category |
| Product Name | Product name |
| Sales | Sales amount |
| Quantity | Quantity ordered |
| Discount | Discount applied |
| Profit | Profit generated |
| Shipping Cost | Shipping cost |
| Order Priority | Order priority |

---

## 🛠️ Technologies Used

- 🐍 Python
- 🐼 Pandas
- 🔢 NumPy
- 📊 Matplotlib
- 🎨 Seaborn
- ☁️ Google Colab
- 📓 Jupyter Notebook
- 📈 Streamlit / Plotly for the dashboard component

---

# 🔍 Data Analysis Workflow

## 1. Data Loading

The Superstore dataset was loaded into a Pandas DataFrame using the `latin1` encoding.

```python
df = pd.read_csv(
    "superstore_dataset2011-2015.csv",
    encoding="latin1"
)
````

---

## 2. Dataset Inspection

The initial dataset contains:

```text
Rows    : 51,290
Columns : 24
```

The dataset includes information related to:

* Orders
* Customers
* Products
* Geography
* Sales
* Quantity
* Discounts
* Profit
* Shipping
* Order priority

---

## 3. Data Types

The original dataset contains:

* **17 object columns**
* **5 float columns**
* **2 integer columns**

The `Order Date` and `Ship Date` columns were converted to proper datetime format for time-series analysis.

---

## 4. Missing-Value Analysis

The main missing-value issue was found in the **Postal Code** column.

| Column            | Missing Values | Missing % |
| ----------------- | -------------: | --------: |
| Postal Code       |         41,296 |    80.51% |
| All other columns |              0 |        0% |

Therefore, **80.51% of Postal Code values are missing**, while the remaining analytical columns contain no missing values.

---

## 5. Duplicate Analysis

The dataset was checked for duplicate rows.

```text
Duplicate rows: 0
```

No duplicate records were found.

After the duplicate-removal step, the dataset remained:

```text
51,290 rows × 24 columns
```

---

# 📅 Feature Engineering

Several additional features were created from the date columns:

* Order Year
* Order Month
* Order Month Name
* Order Quarter
* Shipping Days

These features were used for time-series and shipping analysis.

---

# 📊 Business KPIs

The analysis produced the following overall business metrics:

| KPI                            |              Value |
| ------------------------------ | -----------------: |
| Total Sales                    | **$12,642,501.91** |
| Total Profit                   |  **$1,467,457.29** |
| Total Quantity                 |        **178,312** |
| Total Orders                   |         **25,035** |
| Unique Customers               |          **1,590** |
| Unique Products                |         **10,292** |
| Unique Countries               |            **147** |
| Average Sales / Transaction    |        **$246.49** |
| Average Profit / Transaction   |         **$28.61** |
| Average Discount               |         **14.29%** |
| Average Quantity / Transaction |           **3.48** |
| Overall Profit Margin          |         **11.61%** |

---

# 💰 Sales Analysis

## Sales by Category

The total sales by category were:

| Category        |             Sales |
| --------------- | ----------------: |
| Technology      | **$4,744,557.50** |
| Furniture       | **$4,110,874.19** |
| Office Supplies | **$3,787,070.23** |

Technology generated the highest total sales at **$4.74 million**.

---

## Profit by Category

| Category        |          Profit |
| --------------- | --------------: |
| Technology      | **$663,778.73** |
| Office Supplies | **$518,473.83** |
| Furniture       | **$285,204.72** |

Technology also generated the highest total profit at **$663,778.73**.

---

# 📦 Sub-Category Analysis

The highest-selling sub-categories were:

| Sub-Category |             Sales |
| ------------ | ----------------: |
| Phones       | **$1,706,824.14** |
| Copiers      | **$1,509,436.27** |
| Chairs       | **$1,501,681.76** |
| Bookcases    | **$1,466,572.24** |
| Storage      | **$1,127,085.86** |

Phones generated the highest sales among the 17 sub-categories.

---

# 🌎 Market Analysis

Sales by market:

| Market |             Sales |
| ------ | ----------------: |
| APAC   | **$3,585,744.13** |
| EU     | **$2,938,089.06** |
| US     | **$2,297,200.86** |
| LATAM  | **$2,164,605.17** |
| EMEA   |   **$806,161.31** |
| Africa |   **$783,773.21** |
| Canada |    **$66,928.17** |

APAC recorded the highest sales among the markets analyzed.

---

# 🗺️ Regional Analysis

The highest-sales regions were:

| Region         |             Sales |
| -------------- | ----------------: |
| Central        | **$2,822,302.52** |
| South          | **$1,600,907.04** |
| North          | **$1,248,165.60** |
| Oceania        | **$1,100,184.61** |
| Southeast Asia |   **$884,423.17** |

The **Central region** recorded the highest sales at **$2.82 million**.

---

# 👥 Customer Segment Analysis

Sales by customer segment:

| Segment     |             Sales |
| ----------- | ----------------: |
| Consumer    | **$6,507,949.42** |
| Corporate   | **$3,824,697.52** |
| Home Office | **$2,309,854.97** |

The Consumer segment generated the highest sales at **$6.51 million**.

---

# 📈 Sales Trend Analysis

## Yearly Sales

| Year |             Sales |
| ---- | ----------------: |
| 2011 |   **$895,931.96** |
| 2012 | **$1,006,427.18** |
| 2013 | **$1,341,260.59** |
| 2014 | **$1,621,903.10** |

The yearly analysis shows increasing sales across the four years covered in the dataset.

The highest annual sales were recorded in **2014 at $1.62 million**.

The project also includes:

* Monthly sales trends
* Quarterly sales comparison
* Year-over-year sales visualization

---

# 📱 Top Products by Sales

The highest-selling products in the analysis include:

| Product                               |          Sales |
| ------------------------------------- | -------------: |
| Apple Smart Phone, Full Size          | **$86,935.78** |
| Cisco Smart Phone, Full Size          | **$76,441.53** |
| Motorola Smart Phone, Full Size       | **$73,156.30** |
| Nokia Smart Phone, Full Size          | **$71,904.56** |
| Canon imageCLASS 2200 Advanced Copier | **$61,599.82** |

The **Apple Smart Phone, Full Size** generated the highest sales among individual products at **$86,935.78**.

---

# 💹 Top Products by Profit

The highest-profit products include:

| Product                               |         Profit |
| ------------------------------------- | -------------: |
| Canon imageCLASS 2200 Advanced Copier | **$25,199.93** |
| Cisco Smart Phone, Full Size          | **$17,238.52** |
| Motorola Smart Phone, Full Size       | **$17,027.11** |
| Hoover Stove, Red                     | **$11,807.97** |
| Sauder Classic Bookcase, Traditional  | **$10,672.07** |

---

# ⚠️ Loss-Making Products

The analysis also identified products with negative total profit.

| Product                                   |         Profit |
| ----------------------------------------- | -------------: |
| Cubify CubeX 3D Printer Double Head Print | **-$8,879.97** |
| Lexmark MX611dhe Monochrome Laser Printer | **-$4,589.97** |
| Motorola Smart Phone, Cordless            | **-$4,447.04** |
| Cubify CubeX 3D Printer Triple Head Print | **-$3,839.99** |
| Bevis Round Table, Adjustable Height      | **-$3,649.89** |

The most negative total product profit identified was **-$8,879.97** for the Cubify CubeX 3D Printer Double Head Print.

---

# 🌍 Country Analysis

The highest-sales countries included:

| Country        |             Sales |
| -------------- | ----------------: |
| United States  | **$2,297,200.86** |
| Australia      |   **$925,235.85** |
| France         |   **$858,931.08** |
| China          |   **$700,562.03** |
| Germany        |   **$628,840.03** |
| Mexico         |   **$622,590.62** |
| India          |   **$589,650.10** |
| United Kingdom |   **$528,576.30** |

The United States generated the highest sales among the countries in the dataset.

---

# 🚚 Shipping Analysis

## Shipping Mode

The number of transactions by shipping mode:

| Shipping Mode  | Transactions |
| -------------- | -----------: |
| Standard Class |   **30,775** |
| Second Class   |   **10,309** |
| First Class    |    **7,505** |
| Same Day       |    **2,701** |

Standard Class was the most frequently used shipping mode.

The analysis also included a distribution of shipping days to investigate shipping duration patterns.

---

# 🏷️ Discount Analysis

The dataset has:

* **Average Discount:** 14.29%
* **Minimum Discount:** 0%
* **Maximum Discount:** 85%

The relationship between discount and profit was analyzed using scatter plots and category-level box plots.

---

# 🔗 Correlation Analysis

The correlation analysis produced the following relationships:

| Variable Pair                 | Correlation |
| ----------------------------- | ----------: |
| Sales ↔ Shipping Cost         |    **0.77** |
| Sales ↔ Profit                |    **0.48** |
| Sales ↔ Quantity              |    **0.31** |
| Profit ↔ Shipping Cost        |    **0.35** |
| Discount ↔ Profit             |   **-0.32** |
| Quantity ↔ Profit             |    **0.10** |
| Sales ↔ Discount              |   **-0.09** |
| Shipping Cost ↔ Shipping Days |   **-0.16** |

### Important observations

* **Sales and Shipping Cost** have the strongest positive correlation among the analyzed numerical variables at **0.77**.
* **Sales and Profit** show a positive correlation of **0.48**.
* **Discount and Profit** show a negative correlation of **-0.32**.
* **Sales and Discount** show a weak negative correlation of **-0.09**.

> Correlation indicates statistical association and does not by itself establish causation.

---

# 👤 Top Customers by Sales

The top customers by total sales included:

| Customer           |          Sales |
| ------------------ | -------------: |
| Tom Ashbrook       | **$40,488.07** |
| Tamara Chand       | **$37,457.33** |
| Greg Tran          | **$35,550.95** |
| Christopher Conant | **$35,187.08** |
| Sean Miller        | **$35,170.93** |

Tom Ashbrook recorded the highest total sales among the customers analyzed at **$40,488.07**.

---

# 📊 Visualizations



### Distribution Analysis

* Sales distribution
* Profit distribution
* Quantity distribution
* Sales boxplot
* Profit boxplot

### Category Analysis

* Sales by category
* Profit by category
* Sales by sub-category
* Profit by sub-category

### Geographic Analysis

* Sales by market
* Sales by region
* Top countries by sales

### Customer Analysis

* Sales by customer segment
* Top customers by sales

### Time-Series Analysis

* Yearly sales trend
* Monthly sales trend
* Quarterly sales analysis

### Relationship Analysis

* Sales vs Profit
* Discount vs Profit
* Discount distribution by category
* Correlation heatmap

### Product Analysis

* Top 10 products by sales
* Top 10 products by profit
* Top 10 loss-making products

### Shipping Analysis

* Orders by shipping mode
* Distribution of shipping days

---

# 💡 Key Business Insights



### 1. Technology leads category sales and profit

Technology generated **$4.74M in sales** and **$663.78K in profit**, making it the highest-selling and highest-profit category in this analysis.

### 2. Central is the highest-sales region

The Central region generated **$2.82M in sales**, the highest among the analyzed regions.

### 3. Consumer customers contribute the largest sales volume

The Consumer segment generated **$6.51M in sales**, compared with $3.82M from Corporate and $2.31M from Home Office.

### 4. Sales increased across the analyzed years

Annual sales increased from **$895.93K in 2011** to **$1.62M in 2014**.

### 5. Phones are the highest-selling sub-category

Phones generated **$1.71M in sales**, followed by Copiers at **$1.51M** and Chairs at **$1.50M**.

### 6. Some products generate significant losses

The Cubify CubeX 3D Printer Double Head Print recorded the lowest product-level profit in the analysis at **-$8,879.97**.

### 7. Discounts and profit show a negative correlation

The correlation between Discount and Profit is **-0.32**, indicating a negative statistical association in this dataset. This should not be interpreted as proof that discounts directly cause lower profit.

### 8. Sales and shipping cost have a strong positive association

Sales and Shipping Cost have a correlation of **0.77**, the strongest correlation observed among the analyzed variables.

---

# 📁 Repository Structure

```text
Superstore-Sales-EDA/
│
├── Superstore_Sales_EDA.ipynb
├── README.md
│
├── data/
│   └── README.md
│
├── dashboard/
│   ├── app.py
│   ├── requirements.txt
│   └── README.md
│
└── images/
    ├── sales_distribution.png
    ├── profit_distribution.png
    ├── sales_by_category.png
    ├── profit_by_category.png
    ├── sales_by_region.png
    ├── sales_by_segment.png
    ├── yearly_sales.png
    ├── sales_vs_profit.png
    ├── discount_vs_profit.png
    └── correlation_heatmap.png
```

> The `data/`, `dashboard/`, and `images/` folders can be added as the project is expanded.

---

# ▶️ How to Run the Project

## Option 1 — Google Colab

1. Open `Superstore_Sales_EDA.ipynb`
2. Upload the Superstore dataset when prompted
3. Run the notebook cells sequentially

---

## Option 2 — Jupyter Notebook

Clone the repository:

```bash
git clone https://github.com/Saheli04/Superstore-Sales-EDA.git
```

Navigate to the project directory:

```bash
cd Superstore-Sales-EDA
```

Install the required libraries:

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Open:

```text
Superstore_Sales_EDA.ipynb
```

---

# 📊 Dashboard

A professional interactive **Global Superstore Analytics Dashboard** was also developed using:

* Streamlit
* Plotly
* Pandas
* NumPy

The dashboard provides interactive analysis of:

* Sales
* Profit
* Customers
* Products
* Categories
* Regions
* Markets
* Shipping
* Discounts

Dashboard files can be found in the `dashboard/` directory.

---

# 📌 Project Type

**Exploratory Data Analysis | Data Analytics | Business Intelligence | Data Visualization**

---

# 👩‍💻 Author

## Saheli Debnath

Aspiring **Data Analyst / Data Scientist** with an interest in:

* 📊 Data Analytics
* 🤖 Machine Learning
* 🧠 Deep Learning
* 📈 Data Visualization
* 💼 Business Intelligence
* 🐍 Python
* 📊 Dashboard Development

---

⭐ **If you find this project useful, feel free to explore the repository and connect with me.**

````


After that, **don't create the `data`, `dashboard`, or `images` folders manually yet**. We'll add the actual files one by one so your GitHub repository doesn't contain empty or placeholder folders.

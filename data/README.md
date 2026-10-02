# 📂 Dataset Information

This folder contains documentation related to the dataset used in the Superstore Sales Exploratory Data Analysis project.

## Dataset Used

The project uses the **Global Superstore / Superstore Sales dataset** covering transactional sales data from 2011–2015.

The original dataset contains:

- **51,290 records**
- **24 original columns**

After feature engineering, additional analytical columns were created in the notebook.

## Main Data Categories

The dataset contains information about:

- Orders
- Customers
- Products
- Categories
- Sub-categories
- Countries
- Markets
- Regions
- Sales
- Quantity
- Discounts
- Profit
- Shipping costs
- Order priority

## Important Columns

| Column | Description |
|---|---|
| Order ID | Unique order identifier |
| Order Date | Date of order |
| Ship Date | Date of shipment |
| Customer Name | Customer name |
| Segment | Customer segment |
| Country | Customer country |
| Market | Market |
| Region | Geographic region |
| Category | Product category |
| Sub-Category | Product sub-category |
| Product Name | Product name |
| Sales | Sales amount |
| Quantity | Quantity ordered |
| Discount | Discount applied |
| Profit | Profit generated |
| Shipping Cost | Shipping cost |
| Order Priority | Order priority |

## Data Quality

The analysis found:

- **51,290 rows**
- **0 duplicate rows**
- **41,296 missing Postal Code values**
- **80.51% missing values in Postal Code**
- Other analytical columns did not contain missing values in the initial missing-value analysis.

## Privacy

The dataset is used for educational and analytical purposes. No private or personally sensitive customer information is intentionally added to this repository.

## Note

The raw dataset is not included in this repository at this stage. The notebook can be run by providing the dataset locally or through Google Colab.

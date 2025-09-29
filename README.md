# Exploratory Data Analysis (EDA) on D-Mart Product Data

## 📝 Project Overview

This project performs a comprehensive Exploratory Data Analysis (EDA) on a dataset of products from D-Mart. The primary objectives are to clean the raw data, handle missing values, and extract meaningful insights through statistical summaries and visualizations. The analysis focuses on understanding product pricing, discounts, and category distributions.

The Jupyter Notebook `EDA_Dmart.ipynb` contains all the steps from data loading and cleaning to visualization.

---

## 💾 Dataset

* **Source:** `dMart.xlsx`
* **Description:** The dataset contains various attributes for products available at D-Mart, including:
    * `Name`: Product name
    * `Brand`: Brand of the product
    * `Price`: Original price
    * `DiscountedPrice`: Price after discount
    * `Category` & `SubCategory`: Product categorization
    * `Quantity`: Weight or volume of the product
    * `Description`: Detailed product description

---

## 🛠️ Key Analysis Steps

The analysis is conducted in a systematic manner:

1.  **Data Loading:** The raw data is loaded from `dMart.xlsx` into a pandas DataFrame.

2.  **Data Cleaning & Preprocessing:**
    * **Handling Null Values:** Missing values in the dataset were handled using various strategies:
        * `Name`: Filled based on the product description.
        * `Brand`: Filled with the string "Unknown".
        * `Price` & `DiscountedPrice`: Filled with the median value of the respective columns.
        * `Category`, `SubCategory`, `BreadCrumbs`: Filled with the string "Unknown".
        * `Quantity`: Filled based on values from similar products.
        * `Description`: Filled with the string "Not Available".
    * **Duplicate Check:** The dataset was checked for any duplicate rows (none were found).
    * **Clean Data Export:** The cleaned DataFrame was saved to a new file named `dMart_cleaned.xlsx`.

3.  **Exploratory Data Analysis & Visualization:**
    * **Price Distribution:** A histogram and a boxplot were created to visualize the distribution of product prices and identify outliers.
    * **Price vs. Discounted Price:** A scatter plot was generated to analyze the relationship between the original and discounted prices.
    * **Correlation Analysis:** A heatmap was used to show the strong positive correlation between `Price` and `DiscountedPrice`.
    * **Pairplot:** A pairplot was created to visualize the pairwise relationships between numerical features.
    * **Category Analysis:** The distribution of products across different categories and sub-categories was analyzed using `value_counts()`.

---

## ⚙️ Requirements

To run this notebook, you need to have Python installed along with the following libraries:

* pandas
* numpy
* matplotlib
* seaborn

You can install these libraries using pip:
```bash
pip install pandas numpy matplotlib seaborn openpyxl

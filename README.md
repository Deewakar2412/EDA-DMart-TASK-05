<div align="center">
  <h1 align="center">🛒 D-Mart Product Analysis: An EDA Project 🛒</h1>
  <p align="center">
    An in-depth exploratory data analysis of D-Mart product data to uncover insights into pricing, discounts, and product categories.
  </p>
</div>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python"/>
  <img src="https://img.shields.io/badge/Pandas-2C2D72?style=for-the-badge&logo=pandas&logoColor=white" alt="Pandas"/>
  <img src="https://img.shields.io/badge/Matplotlib-3776AB?style=for-the-badge&logo=matplotlib&logoColor=white" alt="Matplotlib"/>
  <img src="https://img.shields.io/badge/Seaborn-3776AB?style=for-the-badge&logo=seaborn&logoColor=white" alt="Seaborn"/>
  <img src="https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=Jupyter&logoColor=white" alt="Jupyter"/>
</p>

---

## 📝 **Project Overview**

This project performs a comprehensive **Exploratory Data Analysis (EDA)** on a dataset of products from D-Mart. The primary objectives are to clean the raw data, handle missing values, and extract meaningful insights through statistical summaries and visualizations. The analysis focuses on understanding product pricing, discounts, and category distributions.

The Jupyter Notebook `EDA_Dmart.ipynb` contains all the steps from data loading and cleaning to visualization.

---

## 💾 **Dataset**

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

## 🛠️ **Key Analysis Steps**

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

## 📊 **Visualizations**

Several plots were generated to visualize the data, including:
* Histograms and Boxplots for price distributions.
* A Scatter Plot to show the relationship between price and discounted price.
* A Heatmap to display the correlation matrix.
* Count Plots for product categories and top sub-categories.

---

## ⚙️ **Requirements**

To run this notebook, you need to have Python installed along with the following libraries:

* pandas
* numpy
* matplotlib
* seaborn

You can install these libraries using pip:
```bash
pip install pandas numpy matplotlib seaborn openpyxl



---

## 🚀 How to Use

1.  **Clone this repository** to your local machine:
    ```bash
    git clone <your-repository-url>
    ```
2.  **Place the dataset** `dMart.xlsx` in the root directory of the project.
3.  **Open and run** the Jupyter Notebook `EDA_Dmart.ipynb` to see the complete analysis.

The cleaned data will be saved as `dMart_cleaned.xlsx`.

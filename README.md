# Data-Binning-Data-Formatting-using-Python
## Theory
This experiment demonstrates two important data preprocessing techniques: **Data Binning** and **Data Formatting**.

### Data Binning
Binning (also called discretization) is the process of converting continuous numerical data into categorical groups (bins). It helps in:
- Reducing the impact of noise
- Simplifying analysis
- Creating meaningful categories for visualization and modeling

Pandas provides `pd.cut()` for binning:

```python
bins = [0, 10000, 30000, 60000]
labels = ['Low', 'Medium', 'High']
df['Price_Category'] = pd.cut(df['Price'], bins=bins, labels=labels)
```

### Data Formatting
Data formatting involves cleaning and standardizing data for consistency:
- Changing data types (`astype()`)
- Converting text to uppercase/lowercase
- Rounding numerical values
- Renaming or adding columns

Common operations shown:
```python
df['Product'] = df['Product'].str.upper()        # text formatting
df['Price'] = df['Price'].round(2)               # rounding
df['Units_sold'] = df['Units_sold'].astype(float) # type conversion
```

The notebook uses two example datasets:
1. Product sales data (Price and Units_sold)
2. Food delivery orders (Order value, Delivery time, Distance)

## Key Operations Demonstrated

1. Creating a sample DataFrame with product sales data
2. Binning Price into Low/Medium/High categories using `pd.cut()`
3. Binning Units Sold into Less Sold / Moderately Sold / Highly Sold
4. Checking and converting data types with `astype()`
5. Converting product names to uppercase using `.str.upper()`
6. Rounding numerical values
7. Sorting data by a column
8. Displaying unique category values
9. Creating a food delivery dataset and performing similar binning on:
   - Order value (Less / Moderate / High orders)
   - Delivery time (Less / Moderate / High time)
10. Additional formatting and sorting operations

These techniques are essential for:
- Exploratory Data Analysis (EDA)
- Feature engineering in machine learning
- Creating interpretable categories from continuous variables
- Improving data consistency and readability

## Conclusion

The experiment successfully demonstrated how to:
- Perform data binning using `pd.cut()` to convert continuous variables into meaningful categories
- Apply data formatting operations such as type conversion, text standardization, and rounding
- Work with both small custom datasets and realistic scenarios (product sales and food delivery orders)
- Sort data and inspect unique categories after preprocessing

Key outcomes:
- Price and Units Sold were successfully grouped into logical categories
- Order value and Delivery time in the food delivery dataset were binned effectively
- Data formatting improved consistency (uppercase product names, float conversion, etc.)

Data binning and formatting are fundamental preprocessing steps that make raw data more suitable for analysis, visualization, and modeling.

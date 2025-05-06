# zudio Sales Data Analysis
 Nimra Ashraf
# SU92-BSAIM-F24-182

```python
# Install Required Libraries
pip install pandas matplotlib seaborn

# Load Required Libraries
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

# Load Dataset Example
df = pd.read_csv('data.csv')

# Display the first few rows of the dataset
print(df.head())

# Example: Plotting Price vs. Order ID
df[['Price', 'Order ID']].plot(kind='line')
plt.title('Price vs. Order ID')
plt.xlabel('Order ID')
plt.ylabel('Price')
plt.show()

# Example: Resetting Index
df.reset_index(inplace=True)
print("Index has been reset.")

# Data Cleaning Example
# Handling missing values
df.fillna(0, inplace=True)
print("Missing values have been filled.")

# Descriptive Statistics
print("Descriptive Statistics:")
print(df.describe())

# Grouped Data Analysis Example
grouped = df.groupby('Category').sum()
print("Grouped Data by Category:")
print(grouped)

# Visualization Example: Correlation Heatmap
sns.heatmap(df.corr(), annot=True, cmap='coolwarm')
plt.title('Correlation Heatmap')
plt.show()

# Example: Bar Chart of Sales by Category
df.groupby('Category')['Sales'].sum().plot(kind='bar', color='skyblue')
plt.title('Total Sales by Category')
plt.xlabel('Category')
plt.ylabel('Sales')
plt.show()

# Example: Scatter Plot of Price vs. Quantity
df.plot.scatter(x='Price', y='Quantity', alpha=0.5, color='green')
plt.title('Price vs. Quantity')
plt.xlabel('Price')
plt.ylabel('Quantity')
plt.show()

# Example: Saving the cleaned DataFrame
df.to_csv('cleaned_data.csv', index=False)
print("Cleaned data saved to 'cleaned_data.csv'.")
```
https://github.com/AIMA318/pf-project-g
```

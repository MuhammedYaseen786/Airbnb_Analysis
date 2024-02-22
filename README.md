# Airbnb_Analysis
Airbnb Analysis 
# prompt: Airbnb analysis

import pandas as pd

# Read the Airbnb data from a CSV file
df = pd.read_csv("C:\Users\yasee\AppData\Local\Temp\bec6dae9-0eb7-4d7b-bc58-250b245bc6b6_airbnb.csv.zip.6b6\airbnb.csv")

# Show the first few rows of the DataFrame
df.head()

# Print the number of rows and columns in the DataFrame
print(df.shape)

# Show the data types of each column
df.dtypes

# Calculate the average price of an Airbnb listing
average_price = df["price"].mean()
print(f"Average price: ${average_price:.2f}")

# Find the most expensive Airbnb listing
most_expensive = df["price"].max()
print(f"Most expensive listing: ${most_expensive:.2f}")

# Count the number of listings in each neighborhood
neighborhood_counts = df["neighbourhood_group"].value_counts()
print(neighborhood_counts)

# Create a bar chart of the number of listings in each neighborhood
neighborhood_counts.plot(kind="bar")

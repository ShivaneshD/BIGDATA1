# BIGDATA1
Customer Segmentation using Self-Organizing Maps (SOM)

Project Overview
This project performs customer segmentation using Self-Organizing Maps (SOM) on the Online Retail Dataset. The goal is to cluster customers based on their purchasing behavior, which includes features such as purchase frequency and monetary value. The project visualizes the SOM grid through various plots, such as the U-Matrix (distance map) and hit map, providing clear insights into the segmentation.

Dataset

Dataset: Online Retail Dataset
Source: UCI Machine Learning Repository
File Format: .xlsx (Excel)
Size: ~30MB
Columns Used:
CustomerID: Unique customer identifier
Quantity: The quantity of products purchased
UnitPrice: The price per unit for each product
InvoiceDate: The date when the transaction occurred
Features:
PurchaseFrequency: The number of purchases made by each customer.
MonetaryValue: The total money spent by each customer, calculated as Quantity * UnitPrice.

Project Files
1. customer_segmentation_som.py
This is the main execution script for the project. It performs the following tasks:

Data Preprocessing:
Loads the dataset from the Excel file.
Calculates new features: PurchaseFrequency and MonetaryValue.
Normalizes the dataset using MinMaxScaler to ensure uniform scaling.
SOM Initialization and Training:
Initializes the SOM grid and trains it using customer-level data.
Generates the U-Matrix and hit map to visualize the segmentation.
Visualization:
U-Matrix (Distance Map): Displays the distances between the SOM nodes to identify clusters.
Hit Map: Visualizes customer distribution across the SOM grid.
SOM with Markers: A visualization with customer data points marked on the SOM grid, overlaid on the U-Matrix.
Cluster Assignment:
Customers are assigned clusters based on the winning node in the SOM grid.
The clustered data is saved to an Excel file.

install dependencies with
pip install -r requirements.txt


Execution Instructions
Prerequisites:
Python 3.x
All required libraries listed in requirements.txt (Install via pip install -r requirements.txt).
Step-by-Step Execution:
Clone the Repository: First, clone the project repository to your local machine:


git clone <repository-link>
cd <project-directory>
Install Dependencies: Ensure all required Python libraries are installed using:

pip install -r requirements.txt
Place Dataset: Ensure the OnlineRetail.xlsx dataset is placed in the project directory. Alternatively, you can modify the path in the script to the location of your dataset file.

Run the Script: Execute the customer_segmentation_som.py script to generate the customer segmentation visualizations and clusters:

bash
Copy code
python customer_segmentation_som.py
View Outputs: After running the script, the following outputs will be generated in the project directory:

som_umatrix.png: U-Matrix visualization.
som_hitmap.png: Hit map of customer density.
som_customer_segmentation.png: SOM plot with customer markers.
customer_segmentation_som.xlsx: Excel file containing cluster assignments for each customer.

Results and Insights
The Self-Organizing Map successfully clusters customers into different segments based on their purchasing behavior. This clustering can be used to tailor marketing strategies or identify potential high-value customers.

The following visualizations provide insights:

U-Matrix: Helps to visually identify distinct customer clusters.
Hit Map: Illustrates how densely customers are distributed across the SOM grid.
Customer Segmentation Map: Provides a clear view of customer clusters with markers for each customer.
Future Improvements
Additional features such as recency of purchase (RFM analysis) can further improve segmentation.
The SOM grid can be fine-tuned to achieve better clustering by adjusting parameters like sigma and learning_rate

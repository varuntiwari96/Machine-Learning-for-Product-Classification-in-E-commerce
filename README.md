# Machine Learning for Product Classification in E-commerce
# Project Overview
This project focuses on applying machine learning techniques to automate the classification of products in an e-commerce setting. By leveraging product descriptions, images, and other attributes, the project aims to predict key attributes such as top and bottom categories, and primary and secondary colors. The project follows a structured workflow, including data analysis, preprocessing, and model evaluation.
# Workflow
1. Exploratory Data Analysis (EDA)
Conducted EDA to understand the dataset, which consists of 229,624 products across 362 parquet files.
Analyzed key attributes such as:
Product Categories: Top and bottom categories of products.
Color Attributes: Primary and secondary color distributions.
Created visualizations to study the product distribution across categories and colors, providing insights into dataset composition.
2. Data Preprocessing
Text Cleaning:

Removed numbers and special characters from product titles, descriptions, and tags using a custom cleaning function.
Consolidated cleaned text into a single column for further analysis and model input.
Image Preprocessing:

Resized product images to 224x224 pixels for image classification tasks.
Flattened image arrays for compatibility with machine learning models.

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

3. Data Preprocessing
Text Cleaning:

Removed numbers and special characters from product titles, descriptions, and tags using a custom cleaning function.
Consolidated cleaned text into a single column for further analysis and model input.

3. Image Preprocessing:

Resized product images to 224x224 pixels for image classification tasks.
Flattened image arrays for compatibility with machine learning models.

# 3. Machine Learning Models
A. Text Classification Models
Multinomial Naive Bayes (Baseline Model):

Applied for predicting top categories using product titles.
Achieved an F1-score of 65% for top category prediction.
When additional features like tags and descriptions were included, the performance declined to an F1-score of 46%.

Support Vector Machine (SVM):

Used to predict both top and bottom categories.
Trained using Word2Vec-generated word embeddings from the cleaned text data.
Performance was lower than the baseline, with an F1-score of 32% for bottom category prediction.
XGBoost Classifier:

Tested for predicting bottom categories.
Achieved an F1-score of 40%, but performance was not optimal compared to other models.

B. Image Processing Models
Decision Tree Classifier:

Combined text and image features (like product titles and encoded images) to predict primary colors.
Accuracy and F1-score hovered around 19%, likely due to the limited training data.
CNN + ResNet50:

Utilized Convolutional Neural Networks (CNN) alongside the ResNet50 architecture for image-based classification of primary colors.
Achieved similar results to the Decision Tree (F1-score of 18%).

C. Multi-output Prediction
Random Forest Classifier:
Used for simultaneous prediction of multiple attributes (top category, bottom category, primary color, and secondary color).
Achieved an average F1-score of 68.75%, demonstrating potential for multi-attribute classification in e-commerce.

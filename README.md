# ML-Classification

## Introduction

This repository contains examples of best practices for solving Machine Learning Classification problems throughout the entire machine learning product life cycle, from data analysis to placing the final machine learning model in production. The code is organized into Jupyter notebooks, with each notebook focusing on a specific classification technique or dataset.

My goal is to provide a clear and concise set of examples that can help you learn how to effectively tackle classification problems, and to guide you through each step of the process, from data exploration and model training to deployment and monitoring. I believe that understanding the entire process of developing a machine learning model, from data cleaning and preprocessing to deploying and maintaining the model in a production environment, is crucial for creating successful machine learning products.

In addition to the notebooks, I've also included a set of scripts and utilities that can help you automate common tasks in the machine learning product life cycle. These tools are designed to help you streamline your workflow and save time, allowing you to focus on building better models.

Whether you're just getting started with Machine Learning or you're a seasoned practitioner, I believe you'll find something of value in this repository. I encourage you to explore the notebooks, try out the code for yourself, and let me know if you have any questions or feedback.

Happy classifying!

## Dataset

The dataset used in this project is the "Penguins" dataset, which was obtained from OpenML. This dataset contains information about three different species of penguins (Adelie, Chinstrap, and Gentoo) and their physical characteristics such as bill length, flipper length, and body mass.

The penguins dataset is an excellent alternative to the commonly used iris dataset for data exploration and visualization. With 344 rows and 8 columns, it provides enough data for meaningful analysis without being overwhelming. Additionally, the inclusion of multiple species allows for more complex analysis and visualization techniques that cannot be performed on the iris dataset.

## 1 - Preprocessing dataset

The first step in solving a machine learning classification problem is to preprocess the dataset. Using the Pandas library, we load the "penguins.csv" file and then analyze it to determine which features are numerical, which are categorical, and which is the target variable. It's essential to identify and handle any missing values or NaNs in the dataset, either by replacing or removing them. In our case, since there are only a few NaNs, we choose to remove them.

The next critical step is to transform categorical features into numerical ones using OneHotEncoder and scale numerical features using Standarscaler. Additionally, we need to transform the classes present in the target variable into numerical labels using LabelEncoder. After completing these preprocessing steps, we can save the datasets ready for use by the Sklearn machine learning libraries.

## 2 - Classification lab

Once we have preprocessed our penguins dataset, the next step is to train and test various classification models with Sklearn. By loading the dataset in the X and y format, we can create a training set and a testing set, ensuring that our models can generalize to unseen data.

We can then instantiate multiple classification models and fit them to our training set. Some of the models we can use include Logistic Regression, Decision Trees, Random Forests, Support Vector Machines (SVMs), and K-Nearest Neighbors (KNN).

After training the models, we can evaluate their performances on the testing set by calculating metrics such as precision, recall, accuracy, and F1 score. We can then visualize the performance of different models by plotting precision and recall curves, which allow us to compare their performance at different thresholds.

Through this process, we can identify the most promising machine learning models for our dataset and select the one that performs best in terms of precision, recall, and overall accuracy. By selecting the best-performing model, we can build a reliable and effective machine learning classifier that can make predictions in production environments.

## 3 - Model optimization

Once we have identified the most promising model, it's time to integrate it into a pipeline to achieve two results:

1) Transform the input data that we want to predict using our machine learning model.
2) Perform a Grid Search process to search for the best hyperparameters.

By integrating the model into a pipeline, we can streamline the process of making predictions on new data and optimize the model's performance through hyperparameter tuning.

The Grid Search process involves selecting a set of hyperparameters and exhaustively searching for the combination of hyperparameters that result in the best performance of the model. This process can be computationally expensive, but Sklearn provides efficient tools to perform Grid Search on a range of hyperparameters.

Once we have completed this process, we can compare the performance of the base model and the optimized model to see if the hyperparameter tuning has improved the model's performance. This comparison can be done by evaluating metrics such as accuracy, precision, recall, and F1-score.

In summary, model optimization involves integrating the most promising model into a pipeline, performing hyperparameter tuning through Grid Search, and comparing the performance of the base and optimized models. This process can significantly improve the performance of the machine learning model, making it more accurate and suitable for production-level predictions.

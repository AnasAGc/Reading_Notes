# Data Science Primer

## Bird's Eye View

Machine learning is not about algorithms.

When you open a textbook or a university syllabus, you'll often be greeted by a grocery list of algorithms.

This has fueled the misconception that machine learning is about mastering dozens of algorithms. However, it's much more than that  Machine learning is a comprehensive approach to solving problems and individual algorithms are only one piece of the puzzle. The rest of the puzzle is how you apply them the right way.

### What makes machine learning so special?


Machine learning is the practice of teaching computers how to learn patterns from data, often for making decisions or predictions. For true machine learning, the computer must be able to learn patterns that it's not explicitly programmed to identify.

### 3 Elements of Great Machine Learning

* First, even though we are "teaching computers to learn on their own," human guidance plays a huge role.

* The second essential element is the quality of your data.

* One of the most dangerous pitfalls in machine learning is overfitting. An overfit model has "memorized" the noise in the training set, instead of learning the true underlying patterns.

## Exploratory Analysis


The purpose of exploratory analysis is to "get to know" the dataset. Doing so upfront will make the rest of the project much smoother, in 3 main ways:

* You’ll gain valuable hints for Data Cleaning (which can make or break your models).

* You’ll think of ideas for Feature Engineering (which can take your models from good to great).

* You’ll get a "feel" for the dataset, which will help you communicate results and deliver greater impact.

However, exploratory analysis for machine learning should be quick, efficient, and decisive... not long and drawn out! You see, there are infinite possible plots, charts, and tables, but you only need a handful to "get to know" the data well enough to work with it.

## Data Cleaning

The steps and techniques for data cleaning will vary from dataset to dataset. As a result, it's impossible for a single guide to cover everything you might run into. However, this guide provides a reliable starting framework that can be used every time. We cover common steps such as fixing structural errors, handling missing data, and filtering observations.


Data cleaning is one those things that everyone does but no one really talks about. Sure, it’s not the best part of machine learning. And no, there aren’t hidden tricks and secrets to uncover. However, proper data cleaning can make or break your project. Professional data scientists usually spend a very large portion of their time on this step.

### Handle Missing Data

Missing data is a deceptively tricky issue in applied machine learning. First, just to be clear, you cannot simply ignore missing values in your dataset. You must handle them in some way for the very practical reason that most algorithms do not accept missing values. "Common sense" is not sensible here
Unfortunately, from our experience, the 2 most commonly recommended ways of dealing with missing data actually suck.

They are:

* Dropping observations that have missing values

* Imputing the missing values based on other observations

* Dropping missing values is sub-optimal because when you drop observations, you drop information.

The fact that the value was missing may be informative in itself. Plus, in the real world, you often need to make predictions on new data even if some of the features are missing! Imputing missing values is sub-optimal because the value was originally missing but you filled it in, which always leads to a loss in information, no matter how sophisticated your imputation method is.

Again, "missingness" is almost always informative in itself, and you should tell your algorithm if a value was missing. Even if you build a model to impute your values, you’re not adding any real information. You’re just reinforcing the patterns already provided by other features.

### Missing categorical data

The best way to handle missing data for categorical features is to simply label them as ’Missing’!

* You’re essentially adding a new class for the feature.

* This tells the algorithm that the value was missing.

* This also gets around the technical requirement for no missing values.

## Feature Engineering


Feature engineering is about creating new input features from your existing ones. In general, you can think of data cleaning as a process of subtraction and feature engineering as a process of addition. This is often one of the most valuable tasks a data scientist can do to improve model performance, for 3 big reasons:

You can isolate and highlight key information, which helps your algorithms "focus" on what’s important.
You can bring in your own domain expertise. Most importantly, once you understand the "vocabulary" of feature engineering, you can bring in other people’s domain expertise!


Most machine learning algorithms cannot directly handle categorical features. Specifically, they cannot handle text values. Therefore, we need to create dummy variables for our categorical features. Dummy variables are a set of binary (0 or 1) variables that each represent a single class from a categorical feature.

The information you represent is exactly the same, but this numeric representation allows you to pass the technical requirements for algorithms.

### Remove Unused Features

Finally, remove unused or redundant features from the dataset.Unused features are those that don’t make sense to pass into our machine learning algorithms. Examples include:

* ID columns

* Features that wouldn't be available at the time of prediction

* Other text descriptions

Redundant features would typically be those that have been replaced by other features that you’ve added during feature engineering.

## Algorithm Selection

And yes, just 5 for now. Instead of giving you a long list of algorithms, our goal is to explain a few essential concepts (e.g. regularization, ensembling, automatic feature selection) that will teach you why some algorithms tend to perform better than others. In applied machine learning, individual algorithms should be swapped in and out depending on which performs best for the problem and the dataset. Therefore, we will focus on intuition and practical benefits over math and theory.

### Regularization in Machine Learning

* Lasso Regression

    * Lasso, or LASSO, stands for Least Absolute Shrinkage and Selection Operator.

    * Lasso regression penalizes the absolute size of coefficients.
        
    * Practically, this leads to coefficients that can be exactly 0.
        
    * Thus, Lasso offers automatic feature selection because it can completely remove some features.
        
    * the "strength" of the penalty should be tuned.
        
    * A stronger penalty leads to more coefficients pushed to zero.

* Ridge Regression
        
    * Ridge regression penalizes the squared size of coefficients.
        
    * Practically, this leads to smaller coefficients, but it doesn't force them to 0.
        
    * In other words, Ridge offers feature shrinkage.
        
    * Again, the "strength" of the penalty should be tuned.
        
    * A stronger penalty leads to coefficients pushed closer to zero.

* Elastic-Net

    * Elastic-Net penalizes a mix of both absolute and squared size.

    * The ratio of the two penalty types should be tuned.

    * The overall strength should also be tuned.

## Model Training

There are a few key techniques that we'll discuss, and these have become widely-accepted best practices in the field. Again, this mini-course is meant to be a gentle introduction to data science and machine learning, so we won't get into the nitty gritty yet. We have plenty of other tutorials for that.

It might seem like it took us a while to get here, but professional data scientists actually spend the bulk of their time on the steps leading up to this one:

* Exploring the data.

* Cleaning the data.

* Engineering new features.

this is how to set up the entire modeling process to maximize performance while safeguarding against overfitting. We will swap algorithms in and out and automatically find the best parameters for each one.

Split Dataset to train and test parts

Cross-validation is a method for getting a reliable estimate of model performance using only your training data. There are several ways to cross-validate. The most common one, 10-fold cross-validation, breaks your training data into 10 equal parts (a.k.a. folds), essentially creating 10 miniature train/test splits.

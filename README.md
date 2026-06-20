# HotelCancellations_ML_Framework
Project in which we take hotel booking stats to model and predict the possible cancellation of a future bookig.


A machine learning project that predicts whether a hotel booking will be canceled, using only the information available at the time the reservation is made. Completed for PSTAT 131/231 (Machine Learning) at UC Santa Barbara.

Overview

Hotel cancellations are costly: an empty room represents revenue that can never be recovered. This project builds and compares several classification models to predict cancellations in advance, which could help hotels make smarter decisions about overbooking, pricing, and staffing.

The best model — a tuned random forest — achieves a ROC-AUC of 0.93 and 86% accuracy on held-out test data.

Data

The data come from the Hotel Booking Demand dataset (Antonio, Almeida, & Nunes, 2019), which contains 119,390 real bookings from two hotels in Portugal between 2015 and 2017.


Source: Kaggle
Outcome variable: is_canceled (binary)
31 predictors covering booking logistics, guest details, pricing, and deposit policy


See codebook.txt for a full description of every variable.

Methods

The project follows a standard supervised learning workflow:


Exploratory data analysis and data cleaning (missing values, outliers, leakage removal)
An 80/20 stratified train/test split
A preprocessing recipe (dummy encoding, normalization, lumping rare categories)
5-fold cross-validation
Four models fit and compared: logistic regression, elastic net, random forest, and a boosted tree
Final evaluation of the best model on the held-out test set

# PHP2550_Project3

## Title

Transportability Analysis of Prediction Model from Framingham Heart Study to NHANES data 

## Description

Evaluating the transportability and the performance is important when applying a prediction model derived in the source population to the target population, especially when the characteristics of two populations differ. Recently, a method that uses inverse-odds weights to get transported brier score estimate has been developed. In this study, we first examine its performance when transporting a prediction model for CVD risk on Framingham Study to NHANES data, while the population in NHANES seem to be healthier than population in Framingham. The average brier score estimated from imputation are 0.0929 and 0.0563 in NHANES for men and women, compared to 0.1939 and 0.1171 for Framingham. We also conduct a simulation study to evaluate the transportability when only summary statistics of the target population are available. We use two methods, multivariate normal distribution and bootstrapping from the source population, to simulate the individual-level data based on the summary statistics of NHANES. The simulated data from the first method is well-calibrated for the mean statistics, and the other is not calibrated. Multivariate normal has a smaller relative bias (13.47% versus 38.93%) for men in brier scores, while bootstrap is slight better for women (-1.62% versus -1.46%). We conclude that the difference in the oracle and the simulated brier score seems to be associated with the difference in the source and the target brier score, and this impacts differ for different simulation methods.

## Package

R version 4.3.0

* kableExtra (1.3.4)
* MASS (7.3-60)
* mice (3.16.0)
* nhanesA (0.7.4)
* riskCommunicator (1.0.1)
* tableone (0.13.2)
* tidyverse (2.0.0)

## Data

The Framingham data is available from the package riskCommunicator, and the NHANES data is available from the package nhanesA.

## Acknowledgement

This project is a collaboration with Dr. Jon Steingrimsson in the Biostatistics Department (jon_steingrimsson@brown.edu). This project is advised by Dr. Alice Paul (alice_paul@brown.edu)
# PHP2550_Project3

## Title

Transportability Analysis of Prediction Model from Framingham Heart Study to NHANES data 

## Description

Evaluating the transportability and the performance is important when applying a prediction model derived in the source population to the target population, especially when the characteristics of two populations differ. Recently, a method that uses inverse-odds weights to get transported brier score estimate has been developed (Steingrimsson et al. 2023). In this study, we first examine its performance when transporting a prediction model for CVD risk on Framingham Study to NHANES data, while the population in NHANES seems to be healthier than population in Framingham. The average brier scores estimated from imputation are 0.0903 and 0.0474 in NHANES for men and women, compared to 0.1939 and 0.1171 for Framingham. We also conduct a simulation study to evaluate the transportability when only summary statistics of the target population are available. We use two methods, multivariate normal distribution and bootstrapping from the source population, to simulate the individual-level data based on the summary statistics of NHANES. The simulated data from the first method is well-calibrated for the mean statistics, and the other is not calibrated. Multivariate normal has a smaller relative bias (8.34% versus 45.48%) for men in brier scores, while bootstrap is comparable to Multivariate normal for women (15.88% versus 15.2%) but with a smaller MSE. We conclude that the difference in the oracle and the simulated brier score seems to be associated with the difference in the source and the target brier score, and these impacts differ for different simulation methods.

## Main Results

Performance comparison for two simulation methods

<table class="tg">
<thead>
  <tr>
    <th class="tg-baqh"></th>
    <th class="tg-baqh" colspan="2">Men</th>
    <th class="tg-baqh" colspan="2">Women</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-baqh"></td>
    <td class="tg-baqh">Multivariate<br>Normal</td>
    <td class="tg-nrix">Bootstrap</td>
    <td class="tg-baqh">Multivariate<br>Normal</td>
    <td class="tg-nrix">Bootstrap</td>
  </tr>
  <tr>
    <td class="tg-baqh">Bias</td>
    <td class="tg-baqh">0.00753 (0.00016)<br></td>
    <td class="tg-baqh">0.04105 (0.00009)</td>
    <td class="tg-baqh">0.00721 (0.00012) </td>
    <td class="tg-baqh">0.00753 (0.00006)</td>
  </tr>
  <tr>
    <td class="tg-baqh">Relative Bias</td>
    <td class="tg-baqh">8.34%</td>
    <td class="tg-baqh">45.48%</td>
    <td class="tg-baqh">15.2%</td>
    <td class="tg-baqh">15.88%</td>
  </tr>
  <tr>
    <td class="tg-baqh">MSE</td>
    <td class="tg-baqh">0.00008 (&lt;0.00001)</td>
    <td class="tg-baqh">0.00169 (0.00001)</td>
    <td class="tg-baqh">0.00007 (&lt;0.00001)</td>
    <td class="tg-baqh">0.00006 (&lt;0.00001)</td>
  </tr>
</tbody>
</table>

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
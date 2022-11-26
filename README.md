# CLAD panel data MIP estimator in Python

In this repository we implement the MIP (Mixed Integer Programming) estimator for the CLAD (Censored Least Absolute Deviations) problem for panel data with left censoring.
The code is written in Python using the cplex package.

This is an extension of the following repository by Kostas Florios for cross-sectional data:

https://github.com/kflorios/clad-estimator-MIP-inPython


# Instructions
1. Set up CPLEX and the DOcplex Python API.
2. Prepare the data file (data_input.txt) as follows:
The first row should contain the headers. The first column should contain the observation number which takes values from 1 to N*T, where N denotes the number of individuals and T the number of observations per individual. So, the t observation of individual i should be on row i*t+1. The second column contains the left-censored response variable.
3. The panel dimensions (N and T) must be set in the python script.
4. The MIP optimization parameters can be changed in the python script.

# Acknowledgement
This repository is part of a research project was supported by the Hellenic Foundation for Research and Innovation (H.F.R.I.) under the “2nd Call for H.F.R.I. Research Projects to support Post-Doctoral Researchers” (Project Number: 902).


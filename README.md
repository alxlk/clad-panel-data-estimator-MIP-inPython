# CLAD panel data MIP estimator in Python

In this repository we implement the MIP (Mixed Integer Programming) estimator for the CLAD (Censored Least Absolute Deviations) problem for panel data with left censoring.
The code is written in Python using the cplex package.

This is an extension of the following repository by Kostas Florios for cross-sectional data:

https://github.com/kflorios/clad-estimator-MIP-inPython


# Instructions
1. Set up CPLEX and the DOcplex Python API.
2. For a panel with dimensions N by T prepare the data files (y.txt and X.txt) as follows:

The y.txt file contains the response variable "y" and the left-censoring level "yc" which is constant. The individual "id" which takes values 1,2,...,N and the time period "t" which takes values 1,2,...,T is included as the 2nd and 3rd column, respectively. The first column "global_id" acts as a counter for each observation of the panel and takes values 1,2,...,N*T.

The X.txt contains the explanatory variables ("x1" and "x2" in the example dataset). Columns "global_id", "id", "t" is included similarly to the y.txt file.

3. Optimization parameters can be changed in the python script. Specifically, the following parameters can be chosen:
d: upper bound on the absolute value of each slope coefficient
dalpha: upper bound on the absolute value of each fixed effect
mipemphasis: cplex optimization parameter
timelimit: time limit in seconds of the optimization
threds: number of threads to use (0 uses all cores)

# Acknowledgement
This repository is part of a research project was supported by the Hellenic Foundation for Research and Innovation (H.F.R.I.) under the “2nd Call for H.F.R.I. Research Projects to support Post-Doctoral Researchers” (Project Number: 902).


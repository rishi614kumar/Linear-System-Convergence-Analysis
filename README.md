# Linear System Convergence Analysis

This Python project is an attempt to discover optimal matrix structures for fast convergence in solving the linear system *Ax=b* with the Jacobi method.


Matrices downloaded from the [Matrix Market](https://math.nist.gov/MatrixMarket/).



# Table of Contents
- [Usage](#Usage)
- [Notes](#Notes)



# Usage

This project was written using Python 3 and can be ran with Jupyter Notebook. The user can download any matrix from the [Matrix Market](https://math.nist.gov/MatrixMarket/) to use with this program. This program assumes loaded *A* matrices are of dimension n x n.

The gatherData function is the primary function to be used for testing convergence. The user can choose to load a predefined *x* vector (dimension n x 1) or generate a new one for their operations. Using 0.1 for the error threshold, 500 for the number of iterations, and 1 for the power is recommend for relatively fast and accurate results.


# Notes

In order to have fair comparisions and limit long convergences, I decided to create some standards for my tests:

1. The *A* matrix should be n x n.
2. The *x* vector (n x 1) is randomly generated with values from [-10,10] and the *b* vector is computed from the product *Ax*.
3. The Jacobi method will run until ||*Ax<sup>i</sup>* - *b*|| < 0.1 or 500 iterations have passed.

For each trial, I collected:

1. Total number of iterations
2. Convergence time
3. Final value of ||*Ax<sup>i</sup>* - *b*|| (final error)
4. Initial value of ||*Ax<sup>i</sup>* - *b*|| (intial error)
5. Condition number of *A*






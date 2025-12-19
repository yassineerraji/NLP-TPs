# Introduction to Mathematical Optimization

This practical work (TP) introduces core ideas from mathematical optimization through short, hands-on exercises in Python.

## Overview

The notebook focuses on two complementary skills:
- **Analytical work**: compute critical points “by hand” (gradient = 0) and reason about their nature.
- **Visualization**: build intuition by plotting 1D slices and 2D contour lines of functions of two variables.

By the end, you should be able to:
- **Find critical points analytically** for simple bivariate functions
- **Visualize functions** with 1D slices and contour plots
- **Connect derivatives to geometry** (gradient and Hessian interpretation)

## Technologies Used

- **NumPy**: Numerical computing and array operations
- **Matplotlib**: Data visualization and plotting
- **Jupyter Notebook**: Interactive development environment

## Contents

The notebook is organized as follows:
- **Exercise 1**: Analytical determination of critical points for three different functions
- **Exercise 2**: Plotting 1D function slices (fixing one variable or restricting to a line)
- **Exercise 3**: Plotting contour lines (isovalues) and verifying results with gradients/Hessians

## Installation

1. Install the dependencies:

```bash
pip install -r requirements.txt
```

2. Start Jupyter:

```bash
jupyter notebook
```

3. Open the notebook: `Introduction to maths optimisation.ipynb`

## Usage

Run the cells sequentially. Each section builds on the previous one, moving from analytical calculations to plots and then to derivative-based verification.
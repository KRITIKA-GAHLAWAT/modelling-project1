# Rational Fractal Spline - Modeling Project

## 📌 Overview

This project implements **Rational Fractal Splines**, a technique in **fractal interpolation** used for **scientific data approximation**. Unlike classical interpolation methods, fractal interpolation functions (FIFs) provide **scalability and flexibility** through **scaling factors and shape parameters**, ensuring that the interpolated curve maintains properties like **monotonicity, positivity, and convexity**.

## 🚀 Features

- **Fractal Interpolation Functions (FIFs)** using rational cubic splines.
- **Shape-Preserving Interpolation** (Monotonicity, Positivity, Convexity).
- **Automated Scaling Factor & Shape Parameter Computation**.
- **Graph Visualization of Interpolated Curves**.

## 🔢 Mathematical Formulation

Given a dataset **{(xi, fi)}**, the interpolation function **Fi(x, f)** is defined as:

\[
Fi(x, f) = αi f + \frac{pi(x)}{qi(x)}
\]

where **pi(x) and qi(x) are cubic polynomials** ensuring shape preservation.

### **Derivative Conditions**:
Boundary derivatives **di** are computed to maintain smooth transitions between interpolated segments.

\[
di = \frac{∆ihi−1+∆i−1hi}{hi+hi−1}, \quad \text{where} \quad ∆i = \frac{fi+1 - fi}{xi+1 - xi}
\]

### **Monotonicity-Preserving Conditions**:
To ensure monotonicity, scaling factors **αi** and shape parameters **vi, wi** are chosen using:

\[
αi ∈ [0, \mui] \quad \text{where} \quad \mui = \min\left(\frac{aidi}{d1}, \frac{aidi+1}{dn}, \frac{fi+1 - fi}{fn - f1}\right)
\]

## 🛠️ Installation

Clone this repository:

```bash
git clone https://github.com/your-repo/fractal-spline.git
cd fractal-spline

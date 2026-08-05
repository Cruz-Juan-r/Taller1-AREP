# Taller1-AREP

# Stellar Luminosity — Regression from First Principles

This project builds, trains, and compares a linear and a polynomial regression model of
stellar luminosity as a function of stellar mass, implementing prediction, mean squared
error, gradients, and gradient descent from scratch with vectorized NumPy (no
scikit-learn or other ML libraries), in order to understand *how* a regression model
learns from data rather than only how to call one.

## Requirements

- Python 3.9+
- NumPy
- Matplotlib
- Jupyter (to open/run the notebook)

Install with:

```bash
pip install numpy matplotlib jupyter
```

## Running the notebook

1. Clone this repository.
2. Launch Jupyter: `jupyter notebook` (or open the file in JupyterLab / VS Code).
3. Open `stellar_luminosity_hands_on.ipynb` and run all cells from top to bottom
   (Kernel → Restart & Run All).

## Main result

A straight line systematically underfits the mass–luminosity relation in this dataset
(over-predicting at low mass, under-predicting at high mass), while adding mass² as a
second feature lets the same gradient-descent algorithm fit the curvature and reach a
much lower training error. Both models remain reasonable inside the observed mass range
(0.6–2.4 solar masses) but diverge sharply and become untrustworthy when extrapolated far
outside it — a reminder that low training error says nothing about regions the data never
covered.

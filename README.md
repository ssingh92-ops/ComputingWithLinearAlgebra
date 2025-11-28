# Numerical Linear Algebra Experiments

This repository collects small numerical experiments in applied linear algebra and numerical analysis. The notebooks are based on topics from AMATH 352 (Applied Linear Algebra & Numerical Analysis, UW Seattle) and extended into self-contained mini projects.

Each notebook explores a specific numerical question: conditioning, stability of algorithms, empirical time complexity, and basic regression modeling.

---

## Contents

- **Gaussian Pairwise Angles and Linear Transforms**  
  `gaussian_pairwise_angles_and_linear_transforms.ipynb`  
  Studies the distribution of angles between random Gaussian vectors in ℝ¹⁰ and how a structured banded matrix \(A\), and its powers \(A^5\) and \(A^{10}\), distort those angle distributions. Illustrates how linear transforms can create strong alignment and anti-alignment in high dimensions.

- **Gram–Schmidt vs Modified Gram–Schmidt**  
  `gram_schmidt_vs_modifiedgram_schmidt_stability.ipynb`  
  Compares classical Gram–Schmidt (CGS) and modified Gram–Schmidt (MGS) on correlated data. Uses angle histograms and the off-diagonal entries of \(Q^\top Q\) to quantify loss of orthogonality and show the improved numerical stability of MGS.

- **Empirical Complexity of Vector and Matrix Operations**  
  `operation_timing_complexity_vec_mat.ipynb`  
  Implements manual versions of vector–vector, matrix–vector, and matrix–matrix products, then times them for increasing sizes. Fits slopes on log–log plots to empirically recover \(O(n)\), \(O(n^2)\), and \(O(n^3)\) behavior.

- **Vandermonde Least-Squares: Normal Equations vs QR vs `lstsq`**  
  `vandermonde_least_squares_method_comparison.ipynb`  
  Fits noisy polynomial models using three solvers: normal equations (via LU), QR factorization, and `numpy.linalg.lstsq`. Compares relative errors across degrees and noise levels, and relates performance to the conditioning of \(A\) vs \(A^\top A\).

- **Wine Quality Linear Regression**  
  `wine_quality_linear_regression.ipynb`  
  Builds a linear model for wine quality from physicochemical features using least squares with an intercept term. Reports train/test relative error and visualizes predicted vs true quality scores.

---

## Technology

All notebooks use:

- Python 3
- NumPy
- SciPy (for some linear solves and factorizations)
- Matplotlib

You can run them in a standard scientific Python environment (e.g. conda, venv, or JupyterLab).

---

## How to Run

1. Clone the repository:

   ```bash
   git clone https://github.com/<your-username>/<your-repo-name>.git
   cd <your-repo-name>
2. Create and Activate an enviornment (optional but recommended)
  python -m venv .venv
  source .venv/bin/activate      # on macOS/Linux
  # .venv\Scripts\activate       # on Windows
3. Install dependencies:
  pip install numpy scipy matplotlib jupyter
4. Launch Jupyter:
  jupyter notebook
5. Open any .ipynb file and run the cells.

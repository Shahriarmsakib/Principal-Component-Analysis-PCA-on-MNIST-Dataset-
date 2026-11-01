# Principal Component Analysis on Handwritten Digits

![NumPy](https://img.shields.io/badge/NumPy-from%20scratch-013243)
![Type](https://img.shields.io/badge/graduate%20coursework-UC%20Riverside-lightgrey)

This project implements PCA by eigendecomposition of the sample covariance and measures how image-reconstruction error grows as principal components are discarded.

The data are scikit-learn's handwritten digits (`load_digits`, 8×8 images → 64-dimensional vectors), an MNIST-style dataset.

## Steps

1. Vectorize the images and subtract the mean image.
2. Eigendecompose the covariance, R = VΛVᵀ, and inspect the sorted eigenvalue spectrum.
3. Reconstruct each image after zeroing the smallest eigenvalues, and display examples.
4. Measure reconstruction error (MSE) as a function of the number of components removed.

## Result

The eigenvalue spectrum drops off sharply. Removing the smallest components barely changes the reconstruction error, while removing many increases it quickly. Keeping about 55–60 of the 64 components preserves reconstruction quality, a reasonable trade-off between compactness and fidelity.

## Files

| File | Content |
|---|---|
| `PCA .ipynb` | Implementation and plots |
| `PCA_Report.pdf` | Write-up |

## Run

```bash
pip install numpy matplotlib scikit-learn
jupyter notebook "PCA .ipynb"
```

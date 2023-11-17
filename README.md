# Principal Component Analysis (PCA) on MNIST Dataset Readme

## Overview

This project demonstrates my proficiency in data science, particularly focusing on Principal Component Analysis (PCA), applied to the MNIST dataset. The primary objectives are implementing PCA, analyzing eigenvalues, and assessing the impact on image reconstruction by varying the number of principal components.

## Methodology-Implementation

### Preliminaries
- Import MNIST images and vectorize each image in the dataset using Numpy and Matplotlib.
- Compute the mean of the images and subtract it from each image.

### Principal Components Analysis (PCA)
(a) Perform PCA on the covariance matrix \(R = V\Lambda V^T\).
(b) Analyze the eigenvalues in \(\Lambda\) to decide which eigenvalues to retain and which to set to zero.
(c) Reconstruct approximations of each image by removing small eigenvalues and display a couple of reconstructed images.

### Error Analysis
(d) Compute the error between the reconstructed and original images using Mean Squared Error (MSE).

### Sensitivity Analysis
(e) Analyze the impact of different numbers of eigenvalues being zeroed out, providing insights based on the MSE and the number of eigenvectors removed.

## Result Analysis

- The sorted eigenvalues show a clear drop-off, indicating which eigenvalues contribute significantly.
- Reconstructing images with a reduced number of eigenvectors demonstrates that removing a small number has a minimal impact on the error, while larger removals result in increased errors.
- Balancing computational efficiency and accuracy suggests keeping around 55-60 eigenvalues out of the original 64. This choice optimally maintains reconstruction quality.

# Hyperspectral Image Analysis Project
## Description
This project focuses on the analysis of hyperspectral imaging (HSI) data using various machine learning techniques. The project includes tasks such as loading and visualizing hyperspectral data, performing Principal Component Analysis (PCA), and applying clustering algorithms like K-Means. The goal is to understand the underlying patterns in the data, reduce dimensionality, and improve signal-to-noise ratio (SNR).

## Data
The dataset consists of hyperspectral imagery stored in the tait_hsi.hdr file. The data is stored in a 3D NumPy array with dimensions (1039, 1087, 273). Additionally, Sentinel-2 data (sentinel2_rochester.npy) is used for clustering tasks.

## Methods
### 1. Data Preprocessing

- No-Data Handling: Replaced zero or no-data values with np.nan to avoid interference with analysis.

- Stretching Techniques: Applied contrast stretching to enhance image visualization.

- Standardization: Transformed data to have a mean of 0 and a standard deviation of 1 for better analysis.

### 2. Principal Component Analysis (PCA)

- Implemented PCA from scratch to reduce the dimensionality of the hyperspectral data.

- Extracted and visualized the first 10 principal components.

- Analyzed the impact of different principal components on the data.

### 3. Clustering with K-Means

- Implemented K-Means clustering from scratch.

- Applied K-Means to both original and PCA-transformed data.

- Compared clustering results with different numbers of principal components.

### Spectral Analysis

- Analyzed the spectral signatures of different materials (e.g., vegetation, urban areas, water bodies).


## Results
- Data Visualization: Improved contrast and interpretability of hyperspectral imagery after handling no-data points and applying stretching techniques.

- Dimensionality Reduction: Successfully reduced the dimensionality of the data using PCA, retaining the most significant features.

- Clustering: Improved clustering results by applying K-Means to PCA-transformed data, reducing noise and focusing on significant features.

## Usage
### 1. Loading and Visualizing Data

- The script starts by loading the hyperspectral data from the tait_hsi.hdr file.

- It then visualizes the RGB and pseudo NIR-R-G images.

### 2. Principal Component Analysis (PCA)

- The PCA function is implemented to reduce the dimensionality of the data.

- The first 10 principal components are extracted and visualized.

### 3. Clustering with K-Means

- The K-Means clustering algorithm is implemented and applied to both the original and PCA-transformed data.

- The results are visualized and compared.

### Author
Sagar Lekhak

PhD Student, Year II

Chester F. Carlson Center for Imaging Science, Rochester Institute of Technology

### Acknowledgments
Special thanks to the instructor and resources provided by the Rochester Institute of Technology for guidance on this project.
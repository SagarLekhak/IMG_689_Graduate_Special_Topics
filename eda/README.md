# IMG_689_Graduate_Special_Topics

## Sentinel-2 Data Analysis and Spectral Matching
### Description
This project focuses on analyzing Sentinel-2 satellite imagery to detect and classify land cover types such as vegetation, urban areas, and water bodies. The project includes:

1. Data Preprocessing: Handling no-data points, applying stretching techniques, and standardizing data.

2. Statistical Analysis: Calculating band statistics (mean, standard deviation, skewness, kurtosis, etc.) and identifying outliers.

3. Correlation Analysis: Computing and visualizing the correlation matrix between spectral bands.

4. Spectral Matching: Using the Spectral Angle Mapper (SAM) to compare Sentinel-2 data with ECOSTRESS spectral library data for materials like asphalt and Quercus (oak).


### Data
The dataset consists of Sentinel-2A imagery with 12 spectral bands. The data is stored in a 3D NumPy array with dimensions (954, 716, 12). The original data source can be found at NASA Earthdata and data information link : https://www.earthdata.nasa.gov/data/instruments/sentinel-2-msi.

### Methods
1. Data Preprocessing:

- No-Data Handling: Replaced zero or no-data values with np.nan to avoid interference with analysis.

- Stretching Techniques: Applied linear, min-max, percentile, and gamma stretching to enhance image contrast.

- Standardization: Transformed data to have a mean of 0 and a standard deviation of 1 for better visualization and analysis.

2. Statistical Analysis
- Calculated band statistics (mean, standard deviation, skewness, kurtosis, etc.) to understand the distribution of pixel values.

- Identified outliers using z-scores (values outside the range of -3 to +3).

3. Correlation Analysis
- Computed the Pearson correlation coefficient matrix to analyze the linear relationships between spectral bands.

- Visualized pairwise scatter plots and density plots for 10-meter bands (B2, B3, B4, and B8).

4. Spectral Matching
- Downloaded target spectra (asphalt and Quercus) from the JPL Spectral Library.

- Downsampled the ECOSTRESS spectra to match Sentinel-2 bands.

- Used the Spectral Angle Mapper (SAM) to identify the closest matches in the Sentinel-2 data.

- Applied a threshold of 0.2 to detect and represent target pixels in the scene.

### Results
- Data Visualization: Improved contrast and interpretability of Sentinel-2 imagery after handling no-data points and applying stretching techniques.

- Outlier Detection: Identified outliers in different bands, such as urban areas in lower bands and water bodies in higher bands.

- Correlation Analysis: Observed high correlations among certain bands (e.g., Bands 1-5) and weak correlations between others (e.g., Bands 1-5 and Bands 6-10).

- Spectral Matching: Successfully detected vegetation and road regions using SAM, with the 1st closest match showing the highest similarity to the target spectra.
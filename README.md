# IoT Environmental Telemetry Data Clustering

## 1. Project Overview
This project applies Data Preprocessing and Unsupervised Machine Learning techniques to time-series data collected from IoT environmental sensors. The primary objective is to clean high-frequency sensor noise and autonomously segment environmental conditions to support automated monitoring and early warning systems.

## 2. Tech Stack & Tools
- **Language:** Python
- **Libraries:** Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn
- **Data Processing:** IQR Outlier Detection, Rolling Mean Smoothing, MinMaxScaler, One-Hot Encoding
- **Modeling:** K-Means Clustering, Principal Component Analysis (PCA)

## 3. Key Technical Implementations
- **Data Cleaning:** Processed over 405,000 raw time-series records across 3 distinct IoT devices, utilizing statistical IQR thresholds to detect and eliminate 8,656 extreme sensor anomalies.
- **Feature Engineering & Smoothing:** Computed the Magnus-Tetens Dew Point and extracted cyclical temporal features (`hour`, `is_day`). Applied a grouped Rolling Mean (`window=5`) at the device level to smooth sensor fluctuations without cross-device data contamination.
- **Dimensionality Reduction:** Assessed feature multicollinearity via Correlation Heatmaps, actively dropping highly correlated redundant gaseous variables ($r > 0.95$).
- **Transformation:** One-Hot Encoded device identifiers and applied `MinMaxScaler` across all features to ensure Euclidean distance parity for clustering algorithms.

## 4. Clustering Insights & Results
Implemented K-Means Clustering to autonomously profile the data. The optimal number of clusters ($K=3$) was mathematically validated using the Elbow Method and visualized via 2D PCA projection. The model successfully segmented the environment into 3 distinct operational states:
- **Warning State:** Characterized by the highest smoke concentration, indicating potential hazards.
- **Optimal State:** Characterized by lower temperatures and high humidity (cool and damp).
- **Normal State:** Standard environmental baseline with average metrics.

## 5. Contact
- **Author:** Đào Đức Nam
- **Email:** daonam2k5@gmail.com

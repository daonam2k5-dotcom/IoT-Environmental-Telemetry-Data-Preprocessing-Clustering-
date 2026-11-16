# IoT-Environmental-Telemetry-Data-Preprocessing-Clustering-
●	Processed and cleaned over 405,000 raw time-series IoT telemetry records across 3 distinct devices, utilizing statistical IQR thresholds to detect and eliminate 8,656 extreme sensor anomalies.
●	Engineered domain-specific environmental metrics (Magnus-Tetens Dew Point) and temporal features; applied grouped Rolling Mean smoothing (window=5) to reduce high-frequency sensor noise without cross-device contamination.
●	Assessed feature multicollinearity via Correlation Heatmaps to remove redundant gaseous variables (r > 0.95), followed by One-Hot Encoding for device IDs and MinMaxScaler normalization on the final 11 features.
●	Implemented K-Means Clustering (K=3, validated via Elbow Method) to autonomously segment data into 3 distinct operational states (Warning, Optimal, Normal), enabling automated environmental anomaly detection.
●	Utilized: Python, Scikit-learn, Pandas

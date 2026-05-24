# 🧬 Enzyme Substrate Prediction (EC1 to EC6)

This project focuses on the multi-label classification of enzyme substrates, developed during the **Kaggle Playground Series - Season 3, Episode 18**. The model leverages chemical features to predict enzyme categories EC1 and EC2.

### 🚀 Live Demo
Explore the interactive model here: https://huggingface.co/spaces/bdaser/Enzyme_Substrate

### 🛠️ Technical Approach & Feature Engineering
* **Chemical Interaction Ratios**: New features such as `Chi1_valence_ratio` and `Chi2_valence_ratio` were engineered to capture specific molecular interactions.
* **PEOE Structural Aggregations**: Total surface area and charge variance were calculated by aggregating the `PEOE_VSA` feature set.
* **Scaling & Modeling**: `RobustScaler` was employed for feature scaling. The model utilizes an `LGBMClassifier` with `class_weight='balanced'` to handle the multi-label target distribution.

### 📊 Model Performance & Confusion Matrix
The performance metrics highlight the model's proficiency, particularly in identifying EC1 and EC2 classes.

| Class | Precision | Recall | F1-Score |
| :--- | :--- | :--- | :--- |
| **EC1** | 0.78 | 0.70 | 0.74 |
| **EC2** | 0.84 | 0.69 | 0.76 |
| **EC3** | 0.44 | 0.54 | 0.49 |
| **EC4** | 0.44 | 0.63 | 0.52 |
| **EC5** | 0.31 | 0.48 | 0.37 |
| **EC6** | 0.21 | 0.34 | 0.26 |

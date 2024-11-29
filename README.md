# Optoelectronic Current Simulation  

This repository contains the code and resources for the paper:  
**"EcoCurrentNet: An Integrated DNN-CatBoost Model for Predicting Optoelectronic Material Performance Under Varying Conditions"**.  

The study focuses on simulating and predicting the current responses of optoelectronic materials under varying environmental conditions using a hybrid deep learning approach. The repository provides the complete workflow, including data generation, model training, testing, and evaluation.  

---

## Repository Structure  

### 1. Files Overview  
- **`Utils.ipynb`**  
  Contains utility functions for data preprocessing, feature engineering, and environment variable simulations. These modules serve as the foundational tools for preparing input data and applying transformations necessary for model training.  

- **`Test.ipynb`**  
  Includes the implementation of various machine learning models and optimizers. This script is used for testing model performance and identifying the best-performing combination of model architecture and optimization algorithm.  

- **`Models.ipynb`**  
  Implements the five custom-designed models evaluated in the study. Each model is designed to address different aspects of the dataset. Based on the results, the **EcoCurrentNet_V4** model was identified as the best-performing model with an **R² score of 0.996526**.  

- **`EcoCurrentNet.ipynb`**  
  A comprehensive script that integrates the complete training and evaluation process for the final model. This notebook includes:  
  - Model training with the selected architecture (**EcoCurrentNet_V4**).  
  - Performance evaluation and result visualization.  
  - Ablation study comparing **EcoCurrentNet** with other machine learning models.  

### 2. Data Simulation  
The dataset used in this study was generated synthetically to simulate the current responses of optoelectronic materials under diverse environmental conditions. The following 12 parameters were varied to create realistic simulations:  
1. Light intensity  
2. Temperature  
3. Material type  
4. Humidity  
5. Wavelength  
6. Pressure  
7. Thickness  
8. Impurity concentration  
9. Bias voltage  
10. Surface treatment  
11. Electric field strength  
12. Density  

These variables were carefully chosen to represent real-world environmental influences on optoelectronic materials. The synthetic dataset is designed to be both diverse and representative of possible experimental scenarios.  

---

## Key Results  

### EcoCurrentNet_V4 Performance  
- **R² Score**: 0.996526  
- EcoCurrentNet_V4 significantly outperformed other machine learning models tested in the study.  

### Ablation Study Results  
| Model                   | R² Score   |  
|-------------------------|------------|  
| Random Forest           | 0.989263   |  
| Bagging Regression      | 0.988846   |  
| Decision Tree           | 0.978542   |  
| Linear Regression       | 0.968972   |  
| Bayesian Ridge          | 0.968969   |  
| Ridge Regression        | 0.996896   |  
| Support Vector Regression (SVR) | 0.928274   |  
| KNeighbors Regression   | 0.770642   |  

The ablation study demonstrates the robustness and accuracy of **EcoCurrentNet_V4**, highlighting its superiority in modeling complex relationships in the dataset.  

---

## Usage Instructions  

1. **Clone the Repository**  
   ```bash  
   git clone https://github.com/Alvy2024/Optoelectronic-current-simulation.git  
   cd Optoelectronic-current-simulation

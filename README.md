## Predicting Age from Resting-State fMRI

### Introduction
In this project, we utilize resting-state fMRI data to explore brain connectivity patterns and predict age. The dataset used for this analysis consists of functional MRI images, confound variables, and phenotypic information for each subject.

### Usage
To run the code, follow these steps:
1. Install the necessary libraries listed in the requirements.txt file.
2. Clone the repository to your local machine.
3. Execute the provided Python scripts in the given order.

### Code Overview
Here's a breakdown of the main sections of the code:

1. **Importing Libraries**: Importing necessary libraries such as pandas, numpy, matplotlib, seaborn, and nilearn for data manipulation, visualization, and analysis.
   
2. **Exploring the Target Variable (Y)**: Loading the phenotype data, checking for duplicates, data types, and missing values, and visualizing the distribution of the target variable (age).

3. **Loading the Atlas**: Fetching the DiFuMo atlas to extract functional signals from fMRI data. Setting the atlas dimensionality to 64 and fetching the atlas filename.

4. **Extracting Features with Nilearn Masker**: Using a masker to extract functional data within atlas parcels from multiple subjects. Computing a correlation matrix to represent regional coactivation between brain regions.

5. **Preparing Data for Machine Learning**: Splitting the data into training and testing sets, and visualizing the distribution of the target variable in both sets.

6. **Running the Model**: Training a Support Vector Regressor (SVR) model using grid search cross-validation to find the best parameters. Making predictions on the test data and evaluating the model's performance using Mean Squared Error (MSE) and R-squared (R2) score.

7. **Interpreting Model Feature Importance**: Interpreting the feature importance of the SVR model by analyzing the correlation matrix between different brain regions. Visualizing the connectivity matrix and identifying significant correlations.

8. **Plotting Connectome**: Plotting the connectome map to visualize the brain network organization based on the connectivity data.

### Conclusion
This project demonstrates how resting-state fMRI data can be used to predict age and explore brain connectivity patterns. By leveraging machine learning techniques and neuroimaging tools, we gain insights into the functional organization of the brain and its relationship with age-related changes. Further analysis and refinement of the models can lead to advancements in understanding brain development and aging processes.

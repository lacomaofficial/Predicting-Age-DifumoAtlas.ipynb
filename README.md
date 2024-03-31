## Exploring Brain Connectivity Patterns to Predict Age: Insights from Resting-State fMRI Data

### Introduction
In this project, we utilize resting-state fMRI data to explore brain connectivity patterns and predict age. The dataset used for this analysis consists of functional MRI images, confound variables, and phenotypic information for each subject.


### Results

The analysis revealed significant connectivity patterns between the transverse sinus and the inferior occipital gyrus, two brain regions with distinct roles in computational neuroscience.

1. **Transverse Sinus**: While the transverse sinus itself does not perform cognitive functions, variations in its connectivity with other brain regions may indicate underlying physiological processes related to blood flow regulation or vascular health. The positive coefficient (0.4429) suggests that changes in the connectivity strength between the transverse sinus and the inferior occipital gyrus are associated with the outcome of interest, potentially reflecting alterations in brain perfusion or vascular integrity.

2. **Inferior Occipital Gyrus**: This brain region is primarily involved in visual processing, including object recognition, shape perception, and visual motion detection. Dysfunction in the inferior occipital gyrus can lead to visual processing deficits. The bidirectional influence between the inferior occipital gyrus and the transverse sinus, indicated by similar coefficient values, suggests reciprocal interactions or feedback loops between visual processing and vascular dynamics.

In summary, understanding the connectivity patterns between these regions provides insights into the complex interplay between vascular health and visual processing, highlighting the importance of considering both physiological and cognitive factors in computational neuroscience research.


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

![Screenshot 2024-03-31 194615](https://github.com/lacomaofficial/Predicting-Age-DifumoAtlas.ipynb/assets/132283879/b12f8665-c0c0-4f02-af34-397daa73187f)



![image](https://github.com/lacomaofficial/Predicting-Age-DifumoAtlas.ipynb/assets/132283879/7741bf11-51bf-4268-8469-e860e14a48f1)
![image](https://github.com/lacomaofficial/Predicting-Age-DifumoAtlas.ipynb/assets/132283879/e12f9d1d-c90f-4e8a-a8e1-6536a40a4d81)


Comparing Supervised and Semi-Supervised Learning for Satellite Image Classification: Insights from High Confidence Pseudo-Labeling and FixMatch - March 2025
=================================

This repository contains all files, models, and documentation for the final project of DSM500, submitted in March 2025. The project focuses on semi-supervised learning techniques, particularly the use of FixMatch and high-confidence pseudo-labeling for satellite image classification.

Project Description
-------------------
The objective of this project is to explore how modern semi-supervised learning algorithms can improve classification performance using limited labeled data. The methods implemented include:
- Supervised baseline training
- FixMatch algorithm using consistency regularization and threshold-based pseudo-labeling
- High-confidence pseudo-labeling: only samples with model prediction confidence above a threshold are used for learning
- Dataset preparation, splitting, and model comparison

Data Source
-----------
- **EuroSAT Dataset**: [https://www.kaggle.com/datasets/apollo2506/eurosat-dataset](https://www.kaggle.com/datasets/apollo2506/eurosat-dataset)

Data Usage:
- Only **10%** of the dataset was used as **labeled** data for training.
- The remaining 90% was split between **test** and **unlabeled** data.
- For memory and computational efficiency, the **unlabeled set** was **further filtered** to keep only a subset of the highest-value samples.

Project Structure
-----------------
.
├── FixM_Models/                 
│   └── Models trained using FixMatch (strong/weak augmentations + threshold pseudo-labels)
│
├── Initial_Models/             
│   └── Baseline supervised models trained on the labeled 10% subset
│
├── PsudoL_Models/              
│   └── Models trained with high-confidence pseudo-labeling
│
├── SplitDataset/              
│   └── Scripts for splitting the EuroSAT dataset into labeled, unlabeled, and test sets
│
├── DSM500_Final_Mar2025.ipynb   
│   └── Final Jupyter notebook containing training, visualizations, and results
│
├── DSM500_Final_Mar2025.html    
│   └── HTML version of the notebook for easy viewing
│
├── Reproducibility_Notice.docx  
│   └── Steps to reproduce results, environment setup, and seed details
│
├── Some Key Insight_Future Research.docx
│   └── Reflections, results summary, and recommendations for future improvements
│
├── requirements.txt             
│   └── Python dependencies

Environment Setup
-----------------
Install required packages with:

    pip install -r requirements.txt

Developed using Python 3.x and Jupyter Notebook.

Running the Code
----------------
Open and run `DSM500_Final_Mar2025.ipynb` to see the training, evaluation, and visualizations. Ensure dataset structure and paths are preserved as defined in the notebook.

Results Summary
---------------
- FixMatch outperformed baseline supervised learning.
- High-confidence pseudo-labeling showed improvements over fully supervised training.
- The effect of unlabeled data quality and quantity was significant on performance.
- Key metrics and plots are visualized in the notebook and HTML file.

Reproducibility
---------------
See `Reproducibility_Notice.docx` for detailed instructions on replicating results and experimental setup.

License
-------
This project is for academic use and shared under the MIT License unless otherwise noted.

---

Created as part of DSM500 coursework for UoL Data Science and AI Masters.

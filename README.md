# Retrospective Data Curation and Causal Inference Analysis in Delirium Dataset

## Description

The repository contains code for the publication manuscript "**Causal Discovery on the Effect of Antipsychotic Drugs on Delirium Patients in the ICU using Large Observational EHR Dataset**" ([Arxiv Link](https://arxiv.org/abs/2205.01057)). It contains code to extract data cohort from MIMIC-III EHR dataset, and relevant data preprocessing, exploratory, machine learning and causal model analysis. In order to run this, please get access to MIMIC-III dataset from [here](https://physionet.org/content/mimiciii/1.4/).

## Tools Used

- **PostgreSQL:** SQL language to extract dataset from large observational dataset.
- **Python:** Primary programming/scripting language.
- **R:** Supporting programming/scripting language.
- **Jupyter Notebook:** Data science notebook environment, aids in faster iteration of prototype building.
- **Pandas, Scikit-learn:** Data science open-source libraries for data handling and general machine learning models.
- **Do-Why, Causal Fusion, bnlearn:** Causal inference open-source (& proprietary) libraries, for handling structural causal models.

## Folder Structure

```plaintext
.                                  # Main source code repository
|───/                              # All relevant sql files before data extraction
│   ├── 0_sql5-prereq.md           # Prerequisite before main sql files 
│   ├── 1_sql5.md                  # Main sql file
│   └── (*supporting_files*).sql   # Supporting sql files for prerequisite
├── 00_data_preparation.ipynb      # Data cleaning and processing codes
├── 01_exploratory_analysis.ipynb  # Codes for exploratory analysis
├── 02_ml_analysis.ipynb           # Codes for machine learning analysis
├── 03_causal_sla.R                # Codes for causal structure generation, in R
|───/10_graph_output               # Outputs after causal structure generation, saved
│   ├── 0_sql5-prereq.md           # Prerequisite before main sql files 
│   ├── 1_sql5.md                  # Main sql file
│   └── (*supporting_files*).sql   # Supporting sql files for prerequisite
├── 04_causal_estimation.ipynb     # Codes for causal inference analysis
|───/11_results                    # All outputs in figures and plots
├── .gitignore                     # Git ignore file
├── LICENSE                        # Project license
└── README.md                      # Project README file
```

## Getting Started
1. Get access to **MIMIC-III**
2. Run relevant SQL codes to extract MIMIC-Delirium dataset from MIMIC-III (**00_data_preparation** folder)
3. Run **00_data_praparation.ipynb** to format and clean data
4. Run **01_exploratory_analysis.ipynb** to explore the dataset and features
5. Run **02_ml_analysis.ipynb** to explore the dataset using machine learning models and compare
6. Run **03_causal_sla.R** to generate causal structures using diferent structure learning algorithms
7. Run **04_causal_estimation.ipynb** to use causal structures generated and complete causal inference


## Contributing
If you would like to contribute to this project, please feel free to fork and submit pull requests with relevant comments.

## License
This project is licensed under the [License Name] - see the LICENSE file for details.

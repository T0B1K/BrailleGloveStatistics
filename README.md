# BrailleGloveStatistics
[![Convert Jupyter Notebooks to HTML](https://github.com/T0B1K/BrailleGloveStatistics/actions/workflows/deploy.yml/badge.svg)](https://github.com/T0B1K/BrailleGloveStatistics/actions/workflows/deploy.yml) [![pages-build-deployment](https://github.com/T0B1K/BrailleGloveStatistics/actions/workflows/pages/pages-build-deployment/badge.svg)](https://github.com/T0B1K/BrailleGloveStatistics/actions/workflows/pages/pages-build-deployment)


This repository contains code and data for analyzing two studies: one on encoding for different stimuli and another on comparing sequential vs OST encoding for vibration stimuli. The repository includes both the experiment data and questionnaire data from participants.

## Repositories  
- [**BrailleGlove**](https://github.com/T0B1K/BrailleGlove)  
  Contains the code for the **microcontroller** responsible for controlling the Braille glove.  

- [**BrailleGlovePaper**](https://github.com/T0B1K/BrailleGlovePaper)  
  Contains the **research paper**, including details about the **user study** and **evaluation**, written in LaTeX.  

- [**BrailleGloveStatistics**](https://github.com/T0B1K/BrailleGloveStatistics)  
  Contains the **anonymized data** and **statistical analysis** from the user study.  

---

# Internals
## GitHub Page

The plots and code used for both studies in the GitHub pages hosted at https://t0b1k.github.io/BrailleGloveStatistics/. This page was automatically built by converting the Jupyter notebook files to HTML and uploading them through the CI/CD pipeline.
That is responsible for converting the Jupyter notebooks (.ipynb files) to HTML format and uploading them to the GitHub Pages site, making the notebooks and results available for online viewing.


## Folder Structure

- `.github/workflows/deploy.yml`: GitHub Actions workflow for deploying the project.
- `study1/experiment/experiment_data/`: Contains the experiment data files for the first study.
  - `STV.txt`: Data file for the "STV" condition.
  - `VST.txt`: Data file for the "VST" condition.
  - `TSV.txt`: Data file for the "TSV" condition.
  - `...`
- `study1/experiment/study1_experiment.ipynb`: Jupyter notebook that contains the code for analyzing the experiment data for the first study.
- `study1/questionnaire/`: Contains the data and code for analyzing user questionnaire responses for the first study.
  - `study1data.csv`: The raw data collected from user questionnaires for the first study.
  - `study1_questionnaire.ipynb`: Jupyter notebook that contains the code for analyzing the questionnaire data for the first study.
  
- `study2/experiment/experiment_data/`: Contains the experiment data files for the second study.
  - `p1_data.txt`: Data file for Participant 1.
  - `...`
  - `p8_data.txt`: Data file for Participant 8.
- `study2/experiment/study2_experiment.ipynb`: Jupyter notebook that contains the code for analyzing the experiment data for the second study.
- `study2/questionnaire/`: Contains the data and code for analyzing user questionnaire responses for the second study.
  - `study2data.csv`: The raw data collected from user questionnaires for the second study.
  - `study2_questionnaire.ipynb`: Jupyter notebook that contains the code for analyzing the questionnaire data for the second study.

## Study Overview

### Study 1
The first study was conducted to see if there is a difference in using an OST encoding for Vibration, Tapping, or Stroking stimulus.

### Study 2
The second study compares the differences between the sequential and OST encoding for the vibration stimuli.

## Libraries Used

The following libraries were used in this project:

- **pandas**: `import pandas as pd`
  - Used for data manipulation and analysis.
- **matplotlib**: `import matplotlib.pyplot as plt`
  - Used for plotting and visualizations.
- **numpy**: `import numpy as np`
  - Used for numerical operations and array manipulation.
- **seaborn**: `import seaborn as sns`
  - Used for statistical data visualization based on matplotlib.
- **scipy**: `from scipy import stats`
  - Provides functionality for various statistical tests and functions.
  - Specific imports include:
    - `chisquare`: For Chi-Square tests.
    - `multinomial`: For working with multinomial distributions.
    - `kruskal`: For Kruskal-Wallis test.
    - `mannwhitneyu`: For the Mann Whitney U test.

- **statsmodels**: `from statsmodels.stats.multicomp import pairwise_tukeyhsd`
  - Used for performing multiple comparisons (Tukey's HSD,..).
- **sklearn** `from sklearn.decomposition import PCA, from sklearn.metrics.pairwise import cosine_similarity`: 
  - Used for performing the PCA and getting the cosine similarity measure.

## Installation

To set up the environment, just open the Jupyter Notebook files in Google Colab, by pressing the button on top of each file


## Folder Structure Tree
.
├── .github/
│   └── workflows/
│       └── deploy.yml                    # GitHub Actions workflow for deployment
├── study1/
│   ├── experiment/
│   │   ├── study_data/
│   │   │   ├── STV.txt                   # Data file for STV condition
│   │   │   ├── VST.txt                   # Data file for VST condition
│   │   │   └── TSV.txt                   # Data file for TSV condition
│   │   └── study1_experiment.ipynb       # Jupyter notebook for analyzing the experiment data
│   ├── questionnaire/
│   │   ├── study1data.csv                # User questionnaire data
│   │   └── study1_questionnaire.ipynb    # Jupyter notebook for analyzing questionnaire data
├── study2/
│   ├── experiment/
│   │   ├── study_data/
│   │   │   ├── p1_data.txt               # Participant 1 data
│   │   │   ├── p2_data.txt               # Participant 2 data
│   │   │   ├── p3_data.txt               # Participant 3 data
│   │   │   ├── p4_data.txt               # Participant 4 data
│   │   │   ├── p5_data.txt               # Participant 5 data
│   │   │   ├── p6_data.txt               # Participant 6 data
│   │   │   ├── p7_data.txt               # Participant 7 data
│   │   │   └── p8_data.txt               # Participant 8 data
│   │   └── study2_experiment.ipynb       # Jupyter notebook for analyzing the experiment data
│   ├── questionnaire/
│   │   ├── study2data.csv                # User questionnaire data
│   │   └── study2_questionnaire.ipynb    # Jupyter notebook for analyzing questionnaire data
├── README.md                             # Project overview and instructions
└── requirements.txt                      # List of dependencies (for Python environment)

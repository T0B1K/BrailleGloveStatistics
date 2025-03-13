# BrailleGloveStatistics
# Experiment and Questionnaire Analysis Repository

This repository contains code and data for analyzing an experiment and a user questionnaire.

## Folder Structure

- `.github/workflows/deploy.yml`: GitHub Actions workflow for deploying the project.
- `study1/experiment/experiment_data/`: Contains the experiment data files.
  - `STV.txt`: Data file for the "STV" condition.
  - `VST.txt`: Data file for the "VST" condition.
  - `TSV.txt`: Data file for the "TSV" condition.
- `study1/experiment/study1_experiment.ipynb`: Jupyter notebook that contains the code for analyzing the experiment data.
- `study1/questionnaire/`: Contains the data and code for analyzing user questionnaire responses.
  - `study1data.csv`: The raw data collected from user questionnaires.
  - `study1_questionnaire.ipynb`: Jupyter notebook that contains the code for analyzing the questionnaire data.

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
- **statsmodels**: `from statsmodels.stats.multicomp import pairwise_tukeyhsd`
  - Used for performing multiple comparisons (Tukey's HSD).

## Installation

To set up the environment, install the required dependencies by running:

```bash
pip install -r requirements.txt

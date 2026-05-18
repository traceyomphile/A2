# CSC3042F Assignment 2

## Overview
This repository contains the code and data for the CSC3042F Assignment 2 sequence-to-sequence phoneme prediction project.

The main files are:
- `A2.ipynb`: Jupyter notebook with the full implementation, training, evaluation, analysis, and plots.
- `a2-dataset/`: dataset folder containing `g2p_train.csv`, `g2p_val.csv`, and `g2p_test.csv`.
- `Report.pdf`: submission report with detailed analysis of results.

## Setup Instructions

1. Install Python dependencies.
   - Recommended: Python 3.10+ with `torch`, `numpy`, `pandas`, `matplotlib`, `nltk`, and `kagglehub`.
   - Example install command:
     ```bash
     pip install torch numpy pandas matplotlib nltk kagglehub
     ```

2. Ensure the dataset is available locally.
   - The notebook uses `DATA_DIR` to point to the dataset location.
   - By default, `DATA_DIR` is set to the latest downloaded dataset directory from `kagglehub`.
   - If your dataset already exists locally, update `DATA_DIR` in `A2.ipynb` to the local path where `a2-dataset` is stored.

3. Run the notebook.
   - Open `A2.ipynb` in Jupyter or VS Code and execute the cells in order.
   - The notebook reads the files: `g2p_train.csv`, `g2p_val.csv`, and `g2p_test.csv` from the dataset directory.

## Important Note on `DATA_DIR`

The notebook defines a `DATA_DIR` variable that points to the dataset location. If you are using a local dataset copy, change `DATA_DIR` to the path of your local dataset folder. If you leave it unchanged, the notebook will attempt to run with the latest downloaded dataset directory.

Example:
```python
DATA_DIR = "c:/Users/trace/OneDrive - University of Cape Town/CSC3042F/Assignments/A2/a2-dataset"
```

## File Descriptions

- `A2.ipynb`
  - Contains the full assignment implementation.
  - Includes data loading, vocabulary building, custom dataset and collate function, LSTM encoder-decoder models, training loops, evaluation, attention comparison, and result analysis.

- `a2-dataset/g2p_train.csv`
  - Training split for grapheme-to-phoneme learning.

- `a2-dataset/g2p_val.csv`
  - Validation split used for hyperparameter tuning and early stopping.

- `a2-dataset/g2p_test.csv`
  - Test split used for final evaluation and error analysis.

- `Report.pdf`
  - Report document containing detailed analysis, discussion of model variants, and conclusions.

## Running Notes

- The notebook is configured to use GPU if available and falls back to CPU automatically.
- The default batch sizes, learning rate, and model settings are defined in the notebook.
- The report file contains the required detailed analysis of results, including comparisons between no-context, fixed-context, and attention-based models.

## Contact

For questions, refer to the notebook comments or the submission report.

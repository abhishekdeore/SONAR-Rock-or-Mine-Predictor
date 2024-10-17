# SONAR Rock or Mine Predictor

## Project Overview
This project implements a machine learning model to classify SONAR signals as either rocks or mines. It demonstrates the process of data analysis, preprocessing, model training, and evaluation using a SONAR dataset.

## Table of Contents
- [Installation](#installation)
- [Dataset](#dataset)
- [Project Structure](#project-structure)
- [Usage](#usage)
- [Data Preprocessing](#data-preprocessing)
- [Model Training and Evaluation](#model-training-and-evaluation)
- [Results](#results)
- [Contributing](#contributing)

## Installation
```bash
git clone https://github.com/abhishekdeore/SONAR-Rock-or-Mine-Predictor.git
cd sonar-rock-mine-predictor
pip install -r requirements.txt
```

## Dataset
The project uses the SONAR dataset, which contains patterns obtained by bouncing sonar signals off a metal cylinder (mine) and a roughly cylindrical rock at various angles and under various conditions. 

- **Features**: 60 numerical attributes representing sonar frequencies
- **Target**: Binary classification (Rock or Mine)
- **Source**: [Kaggle](https://www.kaggle.com/datasets/mattcarter865/mines-vs-rocks)

## Project Structure
```
sonar-rock-mine-predictor/
│
├── data/
│   └── sonar.csv
├── code/
│   └── Rock OR Mine Prediction.ipynb
├── requirements.txt
└── README.md
```

## Usage
To run the analysis:
1. Open the Jupyter notebook `Rock OR Mine Prediction.ipynb` in the `Code` folder.
2. Run all cells in the notebook sequentially.

## Data Preprocessing
The project implements several data normalization techniques to address skewness in the dataset:
- Z-score scaling
- MinMax scaling
- Box-Cox transformation
- Log transformation
- Square root transformation

After comparison, Box-Cox transformation was found to be most effective in normalizing the data.

## Model Training and Evaluation
- **Algorithm**: Logistic Regression
- **Train-Test Split**: 90-10
- **Evaluation Metric**: Accuracy

## Results
- Initial model (without normalization):
  - Training Accuracy: 83.42
  - Testing Accuracy: 76.19
- Model with Z-score scaling:
  - Training Accuracy: 93.37
  - Testing Accuracy: 80.95
- Model with Box-Cox transformation:
  - Training Accuracy: 87.35
  - Testing Accuracy: 85.71

The Box-Cox transformation significantly reduced the gap between training and testing accuracy, indicating better generalization.

## Contributing
Contributions to this project are welcome! Please fork the repository and submit a pull request with your proposed changes.

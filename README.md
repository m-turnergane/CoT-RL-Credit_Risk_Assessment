# Credit Risk Assessment Agent with Chain of Thought and Reinforcement Learning

## Table of Contents
1. [Introduction](#introduction)
2. [Features](#features)
3. [Requirements](#requirements)
4. [Installation](#installation)
5. [Usage](#usage)
6. [Project Structure](#project-structure)
7. [Methodology](#methodology)
8. [Results and Evaluation](#results-and-evaluation)
9. [Future Improvements](#future-improvements)
10. [Disclaimer](#disclaimer)
11. [Contact](#contact)

## Introduction

This Credit Risk Assessment agent is a Python-based application that leverages advanced machine learning techniques, including Chain of Thought (CoT) reasoning and Reinforcement Learning (RL), to evaluate credit risk. The project aims to provide more transparent, effective, and explainable solutions to the complex task of assessing creditworthiness.

## Features

- **Multiple Assessment Models**: Implements base, Chain of Thought, and Reinforcement Learning-enhanced credit risk assessment models.
- **Explainable AI**: Utilizes Chain of Thought reasoning to provide step-by-step explanations for credit decisions.
- **Adaptive Learning**: Incorporates Reinforcement Learning to improve decision-making over time.
- **Comprehensive Risk Evaluation**: Considers various factors including personal information, financial status, loan details, and credit history.
- **Performance Metrics**: Includes accuracy scoring and detailed classification reports for model evaluation.

## Requirements

- Python 3.7+
- pandas
- numpy
- scikit-learn
- matplotlib (for visualization, if needed)

## Installation

1. Clone the repository:
git clone https://github.com/m-turnergane/CoT-RL-Credit_Risk_Assessment.git
cd credit-risk-assessment

2. Create a virtual environment (optional but recommended):
python -m venv venv
# On Mac use source venv/bin/activate  # On Windows use venv\Scripts\activate

3. Install the required packages:
pip install -r requirements.txt

## Usage

1. Prepare your data:
Ensure your credit risk dataset is in CSV format and includes relevant features (see [Project Structure](#project-structure) for details).

2. Run the main script:
python credit_risk_assessment.py

3. Review the output, which includes model performance metrics and example risk assessments.

## Project Structure

- `credit_risk_assessment.py`: Main script containing model implementations and evaluation code.
- `./credit_risk_dataset.csv`: Dataset for training and testing the models (included in repository).
- `README.md`: This file, containing project documentation.
- `requirements.txt`: List of Python dependencies.

## Methodology

This project implements three main approaches to credit risk assessment:

1. **Base Model (CreditRiskAgent)**: A standard machine learning approach using Random Forest Classifier.

2. **Chain of Thought Model (CoTCreditRiskAgent)**: Enhances the base model with a step-by-step reasoning process, providing explanations for its decisions.

3. **Reinforcement Learning Model (RLCoTCreditRiskAgent)**: Combines the Chain of Thought approach with Reinforcement Learning, allowing the model to adapt and improve its decision-making over time.

Each model considers various aspects of a loan application, including:
- Personal information (age, employment length)
- Financial status (income, home ownership)
- Loan details (amount, purpose, interest rate)
- Credit history (defaults, credit history length)

## Results and Evaluation

The models are evaluated using accuracy scores and detailed classification reports. In our tests, the models achieved an accuracy of approximately 90%, with high precision and recall for loan denial predictions and somewhat lower recall for loan approvals.

Assess CoT and RL-based CreditRiskAgent chain of thought reasoning on an example loan application output example:
CoT Agent Decision: Low Risk - Approve Loan
CoT Agent Thoughts:
- Applicant age: 30 years. Employment length: 5 years. 
- Annual income: $60,000. Home ownership: RENT. Renting, no property asset.
- Loan amount: $10,000. Purpose: PERSONAL. Interest rate: 10.0%. Reasonable interest rate. 
- Default on file: N. Credit history length: 5 years. No defaults on record. 
- Calculated risk probability: 0.05. Low risk.

RL-CoT Agent Decision: approve
RL-CoT Agent Action: approve
RL-CoT Agent Thoughts:
- Applicant age: 30 years. Employment length: 5 years. 
- Annual income: $60,000. Home ownership: RENT. Renting, no property asset.
- Loan amount: $10,000. Purpose: PERSONAL. Interest rate: 10.0%. Reasonable interest rate. 
- Default on file: N. Credit history length: 5 years. No defaults on record. 
- Calculated risk probability: 0.05. Low risk.

Example output:
Base CreditRiskAgent Performance:
Accuracy: 0.9090

Classification Report:

          precision   recall    f1-score   support
0            0.91      0.98      0.94      5072
1            0.90      0.67      0.76      1445

accuracy                         0.91      6517

macro avg    0.90      0.82      0.85      6517
weighted avg 0.91      0.91      0.90      6517

## Future Improvements

1. Address class imbalance in the dataset to improve prediction accuracy for loan approvals.
2. Implement more sophisticated feature engineering techniques.
3. Explore hyperparameter tuning to optimize model performance.
4. Investigate other machine learning algorithms or ensemble methods.
5. Develop a user interface for easy interaction with the models.
6. Incorporate more real-world constraints and regulatory requirements into the decision-making process.

## Access the Dataset on Kaggle

[Credit Risk Dataset]: (https://www.kaggle.com/datasets/laotse/credit-risk-dataset?resource=download)

## Disclaimer

This Credit Risk Assessment tool is for educational and research purposes only. It should not be used as the sole basis for making credit decisions in real-world scenarios. Always consult with qualified financial professionals and adhere to relevant regulations when making credit-related decisions.

## Contact

[Muhammad Turner Gane]
Email: [m.turnergane@gmail.com]
LinkedIn: [(https://www.linkedin.com/in/muhammad-gane/)]
GitHub: [(https://github.com/m-turnergane)]

Feel free to contact me with any questions, suggestions, or feedback about this project.
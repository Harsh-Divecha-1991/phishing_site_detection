# Phishing Site Detection

A machine learning project aimed at detecting phishing websites based on various features extracted from URLs.

## Table of Contents

- [Phishing Site Detection](#phishing-site-detection)
- [Introduction](#introduction)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Dataset](#dataset)
- [Preprocessing](#preprocessing)
- [Modeling](#modeling)
- [Evaluation](#evaluation)
- [Results](#results)
- [How to Use](#how-to-use)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgments](#acknowledgments)

## Introduction

Phishing is a fraudulent attempt to obtain sensitive information by disguising as a trustworthy entity in electronic communications. This project uses machine learning to detect phishing websites by analyzing features extracted from URLs.

## Project Structure

```plaintext
├── data
│   ├── raw                    # Raw data from the source
│   ├── processed              # Processed data after preprocessing
├── notebooks
│   ├── data_preprocessing.ipynb # Jupyter notebook for data preprocessing
│   ├── model_training.ipynb     # Jupyter notebook for model training and evaluation
├── src
│   ├── data_preprocessing.py   # Python script for data preprocessing
│   ├── model.py                # Python script for model creation and training
│   ├── evaluation.py           # Python script for model evaluation
├── models
│   ├── model_checkpoint.pth    # Saved model checkpoint
├── requirements.txt            # List of dependencies
├── README.md                   # Project documentation
```

## Installation
To set up the project locally, follow these steps:

```bash
git clone https://github.com/mungekarkiran/phishing_site_detection.git
cd phishing-site-detection
pip install -r requirements.txt
```

## Dataset
The dataset used for this project consists of URLs labeled as phishing or legitimate. Features were extracted from these URLs to train the model.
- Source: PhishTank Dataset
- Size: Approximately 10,000 URLs
- Preprocessing: Extracted features include length of URL, presence of special characters, domain age, and more.

## Preprocessing
The preprocessing steps include:
- Extracting features from URLs.
- Handling missing data.
- Encoding categorical features.
- Normalizing numerical features.

## Modeling
Various machine learning models were explored, including:
- Logistic Regression
- Random Forest
- Support Vector Machine (SVM)
- Gradient Boosting
- Hyperparameter tuning was performed to optimize the models.

## Evaluation
The models were evaluated using the following metrics:
- Accuracy: Proportion of correctly identified phishing and legitimate sites.
- Precision: The percentage of correctly identified phishing sites among all sites identified as phishing.
- Recall: The percentage of actual phishing sites that were correctly identified.
- F1-Score: The harmonic mean of precision and recall.

## Results
The best-performing model achieved:
- Accuracy: 95%
- Precision: 93%
- Recall: 92%
- F1-Score: 92.5%
These results demonstrate the model's ability to effectively identify phishing sites.

## How to Use
To use the trained model for predicting whether a URL is phishing or legitimate:
```from src.model import load_model, predict
model = load_model('models/model_checkpoint.pth')
url = 'http://example.com'
prediction = predict(model, url)
print(f'The URL is {"Phishing" if prediction else "Legitimate"}')
```

## Contributing
Contributions are welcome! Please follow these guidelines:

1. Fork the repository.
2. Create a new branch (git checkout -b feature/your-feature-name).
3. Make your changes.
4. Commit your changes (git commit -m 'Add feature').
5. Push to the branch (git push origin feature/your-feature-name).
6. Open a pull request.

## License
This project is licensed under the MIT License.

## Acknowledgments
- The creators of the PhishTank dataset.
- Inspiration from various machine learning tutorials and resources.
- Thanks to the contributors who helped in making this project possible.

You can customize the placeholder text such as `your_username`, `PhishTank`, or any other details specific to your project. Once you've done that, you can save this as `README.md` in your GitHub repository.

# Fraud Detection Using Autoencoder and Variational Autoencoder

This project focuses on detecting fraudulent credit card transactions using Autoencoder and Variational Autoencoder (VAE) models. The models are trained on a highly imbalanced dataset and are designed to detect anomalies, which in this case are fraudulent transactions.

## Dataset

The dataset used in this project can be found on [Kaggle](https://www.kaggle.com/mlg-ulb/creditcardfraud) under the title **Credit Card Fraud Detection**. It contains 284,807 transactions with 30 features, and the target variable indicates whether a transaction is fraudulent (Class 1) or non-fraudulent (Class 0).

- **Dataset Path:** The data file `creditcard.csv` should be placed in the following directory: `C:\\Users\\ayush\\Downloads\\archive\\`.

## Project Structure

1. **Data Loading and Preprocessing:**
   - The dataset is loaded and checked for null values.
   - Data normalization is performed to scale all features to the same range.
   - The data is split into non-fraud and fraud classes, followed by splitting into training, validation, and test sets.

2. **Model Implementation:**
   - **Autoencoder:**
     - Built using PyTorch, with an encoder-decoder architecture.
     - Trained on non-fraudulent data to learn the underlying data distribution.
   - **Variational Autoencoder (VAE):**
     - A more complex model that learns a latent representation of the data.
     - Incorporates KL Divergence to ensure a structured latent space.

3. **Threshold Tuning:**
   - The reconstruction loss is used to determine the threshold for classifying transactions as fraud or non-fraud.
   - Precision, recall, and accuracy metrics are calculated to identify the optimal threshold.

4. **Evaluation:**
   - The model's performance is evaluated using accuracy, AUC-ROC, and F1-score.
   - Visualizations include ROC curves and confusion matrices to provide insights into model performance.

## Results

- **Autoencoder:**
  - Accuracy: 99%
  - AUC: 0.80
  - F1-Score (Fraud): 0.61

- **Variational Autoencoder (VAE):**
  - Accuracy: 99%
  - AUC: 0.67
  - F1-Score (Fraud): 0.49

## How to Run

1. Download the dataset from [Kaggle](https://www.kaggle.com/mlg-ulb/creditcardfraud) and place the `creditcard.csv` file in the specified directory.
2. Install the required Python packages using `pip install -r requirements.txt`.
3. Run the Python script to preprocess the data, train the models, and evaluate their performance.

## Conclusion

This project demonstrates the use of Autoencoders and Variational Autoencoders for anomaly detection in a highly imbalanced dataset. The models were trained on non-fraudulent data and were able to identify fraudulent transactions with high accuracy.

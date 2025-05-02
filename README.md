# LLM-Application-in-Healthcare-Using-CNN-and-FineTuned-BioBERT
Fine-Tuned LLM code for Breast Cancer Subtype Classification

📁 Input
breastcancer.csv
Target column: Cancer Type Detailed
Over 36 clinical, genomic, and pathological features used for prediction

🔧 Pipeline Overview
1. Data Load
Upload CSV file via Google Colab's file uploader
Inspect label distribution for Cancer Type Detailed

2. CNN Pipeline (Tabular)
Categorical columns one-hot encoded, numeric columns scaled
Data reshaped into (batch, 1, features) for 1D CNN
Trained 1D CNN with two convolutional layers and adaptive pooling
Evaluates on accuracy, precision, recall, F1

4. BioBERT Pipeline (Textual)
Tabular rows converted to structured text (col: value)
Uses dmis-lab/biobert-base-cased-v1.1 with Hugging Face Trainer API
Tokenization, label encoding, and training via Trainer
Evaluation based on same metrics as CNN

4. Metrics Comparison
Accuracy, Precision, Recall, F1-score for both models
Visualization:
Bar chart comparing metrics
Loss vs Epoch plot

📊 Output
Console output:
Model training logs
Final comparison metrics in a DataFrame
Visualizations:
Performance metric bar chart
Training loss curve (CNN and BioBERT)

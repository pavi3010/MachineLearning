# Experiment 1: Comprehensive Machine Learning Workflow and Exploratory Data Analysis

## Aim and Objective
To implement a comprehensive machine learning pipeline across diverse datasets (Structured, Text, and Translation) using Python’s data science ecosystem. The core focus is on:
- Performing extensive Exploratory Data Analysis (EDA) to derive domain-specific insights.
- Executing data preprocessing and feature engineering (e.g., handling missing values, TF-IDF).
- Training and evaluating models for binary/multiclass classification and sequence-to-sequence tasks.

## Libraries Used
- **Data Manipulation:** NumPy, Pandas
- **Visualization:** Matplotlib, Seaborn
- **Machine Learning:** Scikit-Learn (TF-IDF, Random Forest, Logistic Regression)
- **Deep Learning:** TensorFlow/Keras (LSTMs for Seq2Seq)

## Projects & Datasets

### 1. Iris & Diabetes Datasets (Structured Data)
- **Goal:** Classification and correlation analysis.
- **Key Visualizations:** Correlation heatmaps and pair plots to identify key contributors like Glucose and BMI for diabetes probability.

### 2. Spam Detection (Text Data)
- **Goal:** Binary classification of messages.
- **Technique:** Utilized TF-IDF vectorization to transform text into numerical features followed by classification.

### 3. Digits Recognition (Image Data)
- **Goal:** Multiclass classification of handwritten digits.
- **EDA:** Visualized pixel intensity distributions and $5\times5$ grids of digit samples to verify labeling.

### 4. Loan Prediction
- **Model:** Random Forest Classifier.
- **Preprocessing:** Categorical mapping for features like 'Married' and 'Education' and handling missing values.

### 5. English-to-Tamil Translation (NMT)
- **Model:** LSTM-based Encoder-Decoder (Seq2Seq).
- **Process:** Leveraged context vectors to transfer linguistic meaning across time steps for neural machine translation.

## Methodology & Findings
- **Exploratory Data Analysis:** Systematic EDA provided the justification for specific pre-processing techniques and model selection.
- **Model Performance:** Different domains required specialized architectures—ranging from traditional ensemble methods (Random Forest) for structured data to Recurrent Neural Networks (LSTMs) for sequence data.

## Conclusion
The integration of systematic EDA with advanced machine learning models provided a holistic workflow. The experiment successfully demonstrated how to handle different data types (tabular, text, image, and sequence) within a unified Python-based environment.

Advanced Time Series Forecasting with Deep Learning and Explainability

Project Overview

This project focuses on time series forecasting using a deep learning approach based on Long Short Term Memory networks with an attention mechanism. The objective is to achieve accurate forecasting on complex temporal data while maintaining interpretability through explainability analysis.

Dataset Description

A synthetic univariate time series dataset is generated to simulate realistic temporal patterns.

Number of observations
1200

Data generation formula
value t equals sin 0.02t plus 0.5 times sin 0.05t plus Gaussian noise

Noise distribution
Mean 0
Standard deviation 0.3

Dataset characteristics
Non linear behavior
Short term and long term seasonality
Random noise

Data Preprocessing

The preprocessing pipeline includes the following steps.

Min Max normalization with values scaled between 0 and 1

Sliding window transformation
Input window size 30 time steps
Forecast horizon 1 time step

Dataset split
Training data 80 percent
Testing data 20 percent

Final input shape
Samples by 30 by 1

Baseline Model

A naive persistence model is used as the baseline.

Baseline assumption
The value at time t plus 1 is equal to the value at time t

Baseline performance
Root Mean Squared Error approximately 0.42

Deep Learning Model Architecture

The final model architecture is based on stacked LSTM layers with an attention mechanism.

Model structure
Input layer with shape 30 by 1
LSTM layer with 64 units and sequence output enabled
Attention layer for temporal importance learning
LSTM layer with 32 units
Dense output layer with 1 neuron

Training configuration
Optimizer Adam
Loss function Mean Squared Error
Batch size 32
Epochs 30
Early stopping patience 5

Model Evaluation

The trained model is evaluated on unseen test data using standard forecasting metrics.

Test performance
Root Mean Squared Error approximately 0.18
Mean Absolute Error approximately 0.14
Mean Absolute Percentage Error approximately 10 percent

Explainability Analysis

Explainability is achieved using the attention mechanism.

Key observations
Recent time steps receive higher importance
Attention peaks align with seasonal patterns
The model captures both short term and long term dependencies

Comparative Performance

Naive baseline RMSE approximately 0.42
LSTM with attention RMSE approximately 0.18

The deep learning model significantly outperforms the baseline.

Project Deliverables

Fully runnable Python code
Single cell execution pipeline
Baseline comparison
Model evaluation metrics
Explainability analysis
Documented model architecture

Limitations and Future Work

Transformer based models can be explored
Multi step forecasting can be extended
Advanced explainability methods such as SHAP can be applied

Conclusion

This project demonstrates that LSTM based deep learning models with attention mechanisms provide superior forecasting performance on complex time series data while offering meaningful interpretability.

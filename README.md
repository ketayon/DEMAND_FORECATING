# Quantum Machine Learning Demand Forecasting

This project demonstrates a Quantum Machine Learning (QML) approach to demand forecasting. A quantum kernel-based method is implemented to classify demand as high or low, leveraging Qiskit's quantum kernel training and QSVC (Quantum Support Vector Classifier). Dataset from https://www.kaggle.com/datasets/aswathrao/demand-forecasting
---

## Requirements

### Python Libraries
- `qiskit`
- `qiskit-machine-learning`
- `scikit-learn`
- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
---
### Classification Report
```
Model Accuracy on Training Data: 62.00% 

Root Mean Squared Error (RMSE) on Training Data: 0.79 

Confusion Matrix on Training Data: 
[[ 70 160]
 [ 30 240]]

Classification Report on Training Data:
              precision    recall  f1-score  support
0                 0.700  0.304348  0.424242   230.00
1                 0.600  0.888889  0.716418   270.00
accuracy          0.620  0.620000  0.620000     0.62
macro avg         0.650  0.596618  0.570330   500.00
weighted avg      0.646  0.620000  0.582017   500.00
```


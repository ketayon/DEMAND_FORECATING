# Quantum Machine Learning Demand Forecasting

This project demonstrates a Quantum Machine Learning (QML) approach to demand forecasting. A quantum kernel-based method is implemented to classify demand as high or low, leveraging Qiskit's quantum kernel training and QSVC (Quantum Support Vector Classifier). Dataset from https://www.kaggle.com/datasets/aswathrao/demand-forecasting
---

## Features

- **Quantum Kernel-Based Classification**: Utilizes a parameterized quantum circuit to map classical features to a quantum feature space.
- **Data Preprocessing**: Handles feature scaling and demand classification.
- **Model Training and Optimization**: Implements a quantum kernel trainer with SPSA optimization.
- **Evaluation Metrics**:
  - Balanced Accuracy
  - Classification Report
  - Confusion Matrix
  - Loss Convergence Visualization

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
- `torch`

Install these libraries via pip:
```bash
pip install qiskit qiskit-machine-learning scikit-learn pandas numpy matplotlib seaborn torch
```

---

## Files

1. **`train_0irEZ2H.csv` and `test_nfaJ3J5.csv`**:
   - Training and test datasets, containing features like `total_price`, `base_price`, `is_featured_sku`, and `is_display_sku`.
   - Target variable: `units_sold`.

2. **Python Script**:
   - Preprocesses data, trains the QML model, and evaluates its performance.

3. **Generated Output**:
   - Balanced accuracy score
   - Classification report
   - Confusion matrix heatmap
   - Loss convergence plot

---

## Workflow

1. **Data Preprocessing**:
   - Converts weekly sales data into demand classes based on the median units sold.
   - Scales features using `StandardScaler`.

2. **Quantum Kernel Design**:
   - Constructs a parameterized quantum circuit with 4 qubits and 3 layers.
   - Features are encoded using parameterized rotation gates.

3. **Training**:
   - Optimizes quantum kernel parameters using SPSA (Simultaneous Perturbation Stochastic Approximation).
   - Trains the QSVC model with the optimized kernel.

4. **Evaluation**:
   - Computes balanced accuracy and generates classification metrics.
   - Visualizes model performance using confusion matrix and loss convergence plots.

---

## Results

### Balanced Accuracy Test
**0.85**

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

### Confusion Matrix
Confusion Matrix:
[[15  2]
 [ 4 19]]

---

## Visualization

### Loss Convergence Plot
Tracks the loss during the quantum kernel optimization process, showing training progression.

---

## Conclusion

The Quantum Kernel-Based Model provides robust demand classification with a balanced accuracy of 85%. The loss convergence and classification metrics suggest effective training and generalization, making it suitable for demand forecasting applications.

---

## How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com/your-repo-name/qml-demand-forecasting.git
   cd qml-demand-forecasting
   ```

2. Place your datasets (`train_0irEZ2H.csv`, `test_nfaJ3J5.csv`) in the project directory.

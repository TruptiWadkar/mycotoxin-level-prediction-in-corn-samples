# **Mycotoxin Prediction using MLP Regressor**

## **Project Overview**
This project focuses on predicting DON (deoxynivalenol) concentration in corn samples using a Multi-Layer Perceptron (MLP) Regressor. The dataset consists of hyperspectral imaging data, and we use machine learning techniques for preprocessing, training, and evaluation.

---

## **1. Setup Instructions**

### **1.1 Prerequisites**
Ensure you have **Python 3.7+** installed. Verify by running:
```bash
python --version
```

### **1.2 Create a Virtual Environment (Recommended)**
Run the following commands:
```bash
python -m venv myenv  
source myenv/bin/activate  # On Mac/Linux  
myenv\Scripts\activate  # On Windows  
```

### **1.3 Install Dependencies**
To install all required libraries, run:
```bash
pip install -r requirements.txt
```
If `requirements.txt` is not available, install manually:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn lime
```

---

## **2. Running the Code**

### **2.1 Execute the Main Script**
To train the model and generate results, run:
```bash
python main.py
```

### **2.2 View LIME Explanation (Optional)**
If running in Jupyter Notebook:
```python
exp.show_in_notebook()
```
For a matplotlib-based explanation:
```python
exp.as_pyplot_figure()
plt.show()
```

---

## **3. Repository Structure**
```
/Mycotoxin-Prediction
│── data/
│   ├── MLE-Assignment.csv         # Raw dataset
│── src/
│   ├── preprocessing.py           # Data cleaning & feature engineering
│   ├── model.py                   # Model training & evaluation
│   ├── explainability.py          # LIME-based model interpretation
│── main.py                        # Main script to run the pipeline
│── README.md                      # Setup instructions & project details
│── requirements.txt                # Dependencies list
```

---

## **4. Model Details**

### **4.1 Preprocessing Steps**
- **Handling Missing Values**: Dropped missing data.
- **Feature Scaling**: Standardized features using `StandardScaler`.
- **Train-Test Split**: Data divided into **80% training** and **20% testing**.

### **4.2 Model Architecture**
- **Two hidden layers**: (64, 32) neurons in each layer.
- **Default Activation Function**: ReLU (used by default in MLPRegressor).
- **Default Optimizer**: Adam (default for MLPRegressor).
- **500 maximum iterations**: Ensuring sufficient training time.

### **4.3 Performance Metrics**
- **Mean Squared Error (MSE)**: Evaluates model accuracy.
- **R² Score**: Measures predictive performance.
- **Residual Analysis**: Identifies systematic errors.

### **4.4 Explainability**
- **LIME Analysis**: Identifies most influential features.
- **Feature Importance**: Helps understand model decision-making.

---

## **5. Future Improvements**
- **Feature Engineering**: Extracting more domain-relevant spectral bands.
- **Alternative Models**: Exploring **XGBoost or CNN-based spectral analysis**.
- **Error Handling**: Using ensemble techniques to reduce variance.

This project showcases the potential of hyperspectral imaging in predicting mycotoxin levels and suggests further enhancements for better accuracy.


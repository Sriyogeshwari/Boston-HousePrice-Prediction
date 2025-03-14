# 🏡 Boston Housing Price Prediction  

This project predicts housing prices in Boston using **Linear Regression** and **Ridge Regression**. The dataset is preprocessed, visualized, and analyzed to determine which model performs better.  

---

## ✨ Features  
✅ Handles missing values by filling with mean values  
✅ Encodes categorical **Location** column  
✅ Performs **data visualization** with a correlation heatmap  
✅ Applies **StandardScaler** for feature scaling  
✅ Uses **Linear Regression** & **Ridge Regression** for prediction  
✅ Compares model performance using **MSE** and **R² Score**  

---

## 📦 Prerequisites  
Ensure you have the following installed:  
🔹 **Python 3.x**  
🔹 **Google Colab** (if running online)  
🔹 **Pandas**  
🔹 **Numpy**  
🔹 **Matplotlib**  
🔹 **Seaborn**  
🔹 **Scikit-learn**  

Install dependencies using:  
```sh
pip install pandas numpy matplotlib seaborn scikit-learn
```

---

## ⚡ Running the Project  

1️⃣ **Upload the dataset** (`boston_housing_data.csv`) in Google Colab:  
```python
from google.colab import files
uploaded = files.upload()
```

2️⃣ **Load and preprocess data**  
- The script fills missing values  
- Encodes categorical variables  

3️⃣ **Visualize correlations**  
```python
plt.figure(figsize=(12, 10))
sns.heatmap(numeric_data.corr(), annot=True, cmap="coolwarm")
plt.title("Correlation Heatmap")
plt.show()
```

4️⃣ **Train models & make predictions**  
- **Linear Regression**
- **Ridge Regression** (to reduce overfitting)  

5️⃣ **Compare model performance**  
- Mean Squared Error (MSE)  
- R² Score  

6️⃣ **Plot predictions vs actual prices**  
```python
plt.figure(figsize=(10, 6))
plt.scatter(y_test, lr_predictions, label='Linear Regression', alpha=0.7)
plt.scatter(y_test, ridge_predictions, label='Ridge Regression', alpha=0.7, color='red')
plt.plot([y_test.min(), y_test.max()], [y_test.min(), y_test.max()], '--k', color='black')
plt.xlabel('Actual Prices')
plt.ylabel('Predicted Prices')
plt.title('Predictions vs Actual Prices')
plt.legend()
plt.show()
```

---

## 📂 Project Structure  
```
boston-housing-price-prediction/
│── dataset/
│   ├── boston_housing_data.csv  # 🏡 Housing dataset
│── housing_prediction.ipynb      # 📜 Main Jupyter Notebook
│── README.md                     # 📖 Project documentation
```

---

## 🎯 Results & Conclusion  
📌 **MSE & R² scores** are used to evaluate model performance.  
📌 The model with the **higher R² score** performs better.  
📌 **Conclusion:** The script determines whether **Linear Regression** or **Ridge Regression** gives better results for the dataset.  

---

# 🏗️ **Concrete Compressive Strength Prediction**

This project utilizes a **Deep Learning Neural Network** to predict the compressive strength of concrete. By analyzing the chemical composition and age of the mixture, the model provides a fast and accurate estimation, reducing the need for traditional 28-day physical testing.

## 🚀 Project Overview
In civil engineering, concrete strength is the most important factor. This project automates the prediction process using a 3-layer Artificial Neural Network (ANN).

## 🧠 Key Logic & Methodology
* **Data Auditing:** Performed a full audit of ingredients like Cement, Blast Furnace Slag, and Water to ensure data integrity.
* **Feature Engineering:** * Addressed high skewness (**3.26**) in the **Age** feature by applying a `log1p` transformation.
    * Applied **Standardization** (`StandardScaler`) to bring all features (kg/m³, days) to a common scale with Mean=0 and Std=1.
* **Model Architecture:** * Built using the **Keras Sequential API**.
    * Consists of an input layer (8 features), two hidden dense layers (32 and 16 neurons), and a single output neuron.
    * Uses **ReLU** activation for non-linearity and **Adam** optimizer for efficient weight updates.

## 📊 Performance Results
| Metric | Final Result | Logic |
| :--- | :--- | :--- |
| **R-squared (R2) Score** | **77.59%** | Indicates that the model explains ~78% of the variance in concrete strength. |
| **Mean Absolute Error (MAE)** | **5.73 MPa** | On average, the model's predictions are within ~5.7 units of the actual strength. |

## 🛠️ Tech Stack
* **Language:** Python [cite: 
* **Frameworks:** TensorFlow, Keras 
* **Data Processing:** Pandas, NumPy, Scikit-Learn 
* **Visualization:** Matplotlib, Seaborn 

## ☁️ **Deployment Plan**
The final model is designed to be saved as an `.h5` file and is ready for deployment on cloud platforms like **AWS, GCP, or Azure**.

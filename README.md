
# An Advanced Deep Learning-Based Approach for Predicting Photovoltaic Cell Generation

## 📌 Overview
This project presents a **hybrid deep learning framework** for forecasting solar photovoltaic (PV) energy generation using weather and environmental parameters. 
The proposed methodology integrates feature selection, deep learning architectures (LSTM, GRU, Transformer), and ensemble techniques (MLP, CNN, Attention, Simple Mean) to enhance prediction accuracy.

The study uses a publicly available **Kaggle dataset** containing PV energy and weather data to demonstrate the effectiveness of the approach.

---

## 🚀 Key Features
- **Feature Selection** using correlation matrix & backward feature selection to handle multicollinearity.
- **Base Models**:
  - Long Short-Term Memory (**LSTM**)
  - Gated Recurrent Unit (**GRU**)
  - **Transformer** architecture for capturing long-range dependencies.
- **Ensemble Models**:
  - Multi-Layer Perceptron (**MLP**)
  - Convolutional Neural Network (**CNN**)
  - Multi-Head Attention
  - Simple Mean Aggregation
- **Performance Metrics**:
  - Mean Absolute Error (MAE)
  - Mean Squared Error (MSE)
  - Root Mean Squared Error (RMSE)

---

## 📊 Dataset
- **Source**: [Kaggle PV Energy Dataset](https://www.kaggle.com/)  
- **Frequency**: 15-minute intervals
- **Key Features**:
  - Global Horizontal Irradiance (GHI)
  - Temperature (°C)
  - Atmospheric Pressure (hPa)
  - Humidity (%)
  - Wind Speed (m/s)
  - Cloud Coverage (%)
  - Sunlight Time, Day Length
  - Energy Delta [MWh] (target variable)

---

## ⚙️ Methodology
1. **Data Preprocessing**
   - Missing value handling
   - Feature normalization
   - Correlation analysis & redundant feature removal
2. **Base Model Training**
   - Sequence generation with a 60-step sliding window
   - Training GRU, LSTM, Transformer models
3. **Ensemble Learning**
   - Combine base model predictions into a secondary dataset
   - Apply MLP, CNN, Attention, and Mean aggregation
4. **Evaluation**
   - Compare individual vs. ensemble models using MSE, MAE, RMSE

---

## 📈 Results
| Model                   | MSE         | MAE         | RMSE        |
|------------------------|-------------|-------------|-------------|
| GRU                    | 7.74e-8     | 1.49e-4     | 2.78e-4     |
| LSTM                   | 8.32e-8     | 1.55e-4     | 2.88e-4     |
| Transformer            | 4.09e-8     | 1.37e-4     | 2.02e-4     |
| **MLP Ensemble**       | **2.99e-8** | **9.06e-5** | **1.73e-4** |
| CNN Ensemble           | 7.66e-8     | 1.90e-4     | 2.76e-4     |
| Simple Mean Ensemble   | 5.47e-8     | 1.16e-4     | 2.33e-4     |
| Attention Ensemble     | 5.01e-8     | 1.68e-4     | 2.39e-4     |

**Key Insight**: The **MLP-based Ensemble** achieved the best performance.

---

## 🖼 Visualizations
- Correlation heatmaps for feature selection
- Prediction vs. Actual PV generation plots
- Daily mean energy generation comparisons
- Bar plots for error metrics

---

## 📂 Project Structure
```
📦 PV_Forecasting_Project
 ┣ 📜 data_preprocessing.py
 ┣ 📜 train_gru.py
 ┣ 📜 train_lstm.py
 ┣ 📜 train_transformer.py
 ┣ 📜 ensemble_models.py
 ┣ 📜 evaluation.py
 ┣ 📜 utils.py
 ┣ 📊 results/
 ┗ 📄 README.md
```

---

## 🔮 Future Work
- Integrating **hybrid deep learning architectures**
- Including **external weather APIs** for real-time forecasting
- Applying **explainable AI (XAI)** for better interpretability

---

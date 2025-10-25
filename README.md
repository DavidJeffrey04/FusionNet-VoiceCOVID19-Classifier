# Fusion-Net: Voice-Based COVID-19 Classifier

Fusion-Net is a **weighted ensemble of GRU models** developed to classify COVID-19 patients using **voice recordings** from the [Coswara Dataset](https://github.com/iiscleap/Coswara-Data).  
Each GRU model specializes in one sound type — *breathing, cough, vowel pronunciation, and counting*.  
Their outputs are fused via a final neural layer (Fusion-Net) for robust decision-making.

---

## 📘 Overview
| Component | Description |
|------------|-------------|
| Dataset | Coswara voice dataset (IISc Bangalore) |
| Models | Vanilla RNN, LSTM, GRU, and proposed Fusion-Net |
| Task | Binary classification: COVID-positive / COVID-negative |
| Features | Log-Mel spectrograms with Δ and Δ² features |
| Framework | PyTorch |
| Metrics | Accuracy, Precision, Recall, F1-score |

---

## Dataset
- Download it from [Coswara Dataset](https://github.com/iiscleap/Coswara-Data). 
- Only used Positive and Negative classes, Uncertain class was removed due to insufficient samples.

## 📊 Results

### 🧩 Confusion Matrix
<table>
  <tr>
    <td align="center"><b>Fusion-Net Confusion Matrix</b></td>
    <td align="center"><b>GRU Confusion Matrix</b></td>
  </tr>
  <tr>
    <td><img src="Results/Fusion-Net Confusion Matrix.png" alt="Fusion-Net Confusion Matrix" width="600"/></td>
    <td><img src="Results/GRU Confusion Matrix.png" alt="GRU Confusion Matrix" width="600"/></td>
  </tr>
</table>


### 📈 Classification Report
<table>
  <tr>
    <td align="center"><b>Fusion-Net Classification Report</b></td>
    <td align="center"><b>GRU Classification Report</b></td>
  </tr>
  <tr>
    <td><img src="Results/Fusion-Net Classification Report.png" alt="Fusion-Net Classification Report" width="600"/></td>
    <td><img src="Results/GRU Classification Report.png" alt="GRU Classification Report" width="600"/></td>
  </tr>
</table>


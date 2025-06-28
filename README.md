# Bitcoin Price Movement Prediction 📈

This project predicts whether the Bitcoin price will increase the next day using historical price and volume data, along with technical indicators.

---

## 📌 Problem Statement

> Can we predict if the Bitcoin price will go up tomorrow using technical and historical features?

---

## 📊 Features

- `price`, `price_change_pct`, `price_lag_1`, `price_lag_2`
- Rolling metrics: `rolling_mean_3`, `rolling_std_3`
- Volume metrics: `volume`, `volume_lag_1`, `volume_change_pct`
- Technical Indicators:
  - RSI (`rsi_14`)
  - MACD & Signal Line (`macd`, `macd_signal`, `macd_hist`)
  - OBV (`obv`)
  - Moving averages: `volume_ma_3`, `volume_ma_7`
  - Bollinger Bands: `bb_upper`, `bb_lower`, `bb_ma_20`
  - SMA/EMA: `sma_7`, `ema_7`
  - ROC & Momentum

---

## 🧠 Models Used

| Model               | Precision | Recall | F1 Score | Accuracy |
|--------------------|-----------|--------|----------|----------|
| Logistic Regression| ~0.53     | ~0.21  | ~0.30    | ~0.51    |
| XGBoost            | ~0.54     | ~0.21  | ~0.31    | ~0.51    |
| **Random Forest**  | **0.80**  | **0.24**| **0.37** | **0.58** |

✅ Final model: **RandomForestClassifier** with selected features

---

## 📦 Requirements

```bash
pip install -r requirements.txt

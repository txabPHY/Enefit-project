# Predicting the Energy Behaviour of Prosumers
  
We forecast the hourly energy production and consumption of prosumers in Estonia, using data from the Kaggle competition [Enefit: Predict Energy Behavior of Prosumers](https://www.kaggle.com/competitions/predict-energy-behavior-of-prosumers). The slides in `Predict Energy Behavior of Prosumers.pdf` cover the project in more detail.
 
## Models
 
- **LightGBM** on the full dataset, with SHAP for feature importance
- **GRU** (PyTorch) for a single prosumer's production
- **Transformer** (PyTorch) for single prosumer time series forecasting
## Results
 
| Model | Data | MAE | R² |
| --- | --- | --- | --- |
| LightGBM | All prosumers, production | 11.97 | 0.988 |
| LightGBM | All prosumers, consumption | 30.47 | 0.997 |
| GRU | Single prosumer, production | 5.02 | 0.879 |
 
LightGBM worked best across the full dataset. The GRU and transformer were more useful for forecasting individual prosumers.
 
## Files
 
| File | Description |
| --- | --- |
| `data_merger.ipynb` | Merges the datasets and creates features |
| `dataplot.ipynb` | Exploratory plots |
| `lgbm stuff.ipynb` | LightGBM, XGBoost and SHAP analysis |
| `GRU.ipynb` | GRU model |
| `timeseries_transformer.ipynb` | Transformer and model comparisons |
 
## License
 
MIT

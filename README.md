# 🛰️ Meteorite Risk Zone Predictor 🌍☄️

This project uses a ConvLSTM2D deep learning model to predict future meteorite impact risk zones on Earth using historical meteorite landing data from NASA. The predictions are visualized over satellite imagery with Plotly and Mapbox.

---

## 🔍 Overview

Every meteorite that strikes Earth is recorded with a location and time. Using this data, we:
- Convert it into a spatio-temporal tensor grid (latitude × longitude × time)
- Train a deep learning model (ConvLSTM2D) to detect patterns in space and time
- Predict where and when the next high-risk meteorite landing zones could occur
- Overlay the predicted risk zones on an interactive satellite map

---

## 🧠 Model Architecture

- **Input**: A sequence of 2D meteorite heatmaps (by decade)
- **Model**: 2-layer `ConvLSTM2D` followed by spatial convolution
- **Output**: Predicted 2D risk map for the next future frame (next decade)
- **Loss**: Mean Squared Error (MSE)

---

## 📂 Files

- `Meteorite_Satellite_Risk_Map.ipynb` - Fully integrated Google Colab notebook:
  - Preprocessing, model training, prediction, visualization
- `Meteorite_Landings.csv` - Input data (user must upload)
- `newplot.png` - Static snapshot of the final satellite prediction map
  - 🔒 Note: Plotly's satellite tile rendering **won’t show in GitHub preview** due to token access rules.
    This PNG serves as a visual proxy.

---

## 🌍 Map Visualization Notes

- The notebook uses **Plotly + Mapbox** for interactive map rendering.
- You will see the map **live in Google Colab**, but **not in GitHub previews** because:
  - GitHub blocks Plotly's Mapbox rendering in notebooks
  - Mapbox satellite requires authenticated browser access
- To solve this, a static snapshot is included (`newplot.png`)

---

## 🧪 How to Use

1. Open [Google Colab](https://colab.research.google.com/)
2. Upload:
   - `Meteorite_Satellite_Risk_Map.ipynb`
   - `Meteorite_Landings.csv` when prompted
3. Run the notebook from top to bottom
4. View:
   - Model predictions in 2D heatmaps
   - Animated gif of meteorite evolution (`meteorite_risk_timelapse.gif`)
   - Live satellite risk map (Plotly)

---

## 🔐 Mapbox Token

- This project uses a **free Mapbox public token** to render the satellite maps.
- You can replace the token with your own for more control or higher request limits:
  https://account.mapbox.com/access-tokens/

---

## 📝 License

MIT License — free to use, modify, and distribute.

---

## 🙏 Acknowledgements

- NASA Open Data Portal – Meteorite Landings Dataset
- TensorFlow/Keras – Deep Learning Framework
- Plotly + Mapbox – Satellite Visualization Tools

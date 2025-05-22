# Meteorite Risk Zone Predictor 🌍☄️

This project uses a ConvLSTM2D deep learning model to predict future meteorite impact risk zones on Earth, based on historical meteorite landing data from NASA.

## Features
- Convert global meteorite landing data into a spatio-temporal heatmap
- Train a deep learning model (ConvLSTM2D) to learn historical impact patterns
- Predict future high-risk zones
- Visualize risk zones on a global satellite map using Plotly + Mapbox

## Setup
This project is built for Google Colab. Just upload the provided notebook and run it.

## Files
- `Meteorite_Satellite_Risk_Map.ipynb` — Full Colab-ready notebook
- `Meteorite_Landings.csv` — Upload this file when prompted in the notebook

## Mapbox Token
A valid Mapbox token is embedded to render the satellite view. Replace it with your own if needed.

## License
MIT License

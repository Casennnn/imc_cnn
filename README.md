# README

## Overview

This repository contains three Jupyter Notebook files designed for processing time series data, training a convolutional neural network (CNN), and visualizing the results. The project focuses on identifying local peaks and troughs in the data using various features and neural network techniques. It is my personal work during the [IMC Prosperity3 Challenge](https://prosperity.imc.com/).

## Files

1. **dataprocessing.ipynb**
   - This notebook converts raw data into a rolling window format and extracts time series features, resulting in a shape of (30, 4).
   - It identifies local peaks and labels the training output as 0 (trough) or 1 (peak) based on the data's behavior.
   - The four features used for input are:
     - `weighted_avg`
     - `bidask`
     - `RSI`
     - `MACD`
   - Additionally, scaling is performed within the same window to standardize the data.

2. **cnn.ipynb**
   - This notebook trains a CNN model using `tensorflow.keras`.
   - The architecture includes:
     - Two convolutional layers
     - One pooling layer
     - One additional convolutional layer
     - One pooling layer
     - Two dense layers with a sigmoid activation function in the final layer
   - The model is designed to classify the input data based on the features processed in the previous notebook.

3. **datagraph.ipynb**
   - This notebook visualizes the training data, highlighting where peaks and troughs are defined.
   - It takes the trained model and passes in new data to visualize its output in the last cell, allowing for an assessment of the model's performance.

## Dependencies

To run the notebooks, you need to have the following libraries installed:

```bash
pip install tensorflow

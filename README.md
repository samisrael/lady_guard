# lady_guard


This repository contains a machine learning project aimed at predicting the safety levels of various routes based on several geographical and infrastructural features. The project utilizes both Random Forest and Neural Network models to classify routes into three safety levels: Safe, Medium, and Dangerous.

## Table of Contents
- [lady\_guard](#lady_guard)
  - [Table of Contents](#table-of-contents)
  - [Overview](#overview)
  - [Installation](#installation)
  - [Usage](#usage)
  - [Dataset](#dataset)
  - [Models](#models)
  - [Results](#results)

## Overview

The project is designed to analyze the safety of different routes using features such as crime frequency, street lighting, pedestrian traffic, and more. The aim is to provide a tool for urban planners and the general public to make informed decisions regarding route safety.

## Installation

To run this project, you will need Python 3.x and the following libraries:

- `pandas`
- `scikit-learn`
- `tensorflow`
- `folium`

You can install the required libraries using pip:

```bash
pip install pandas scikit-learn tensorflow folium
```

## Usage
1. Clone the repository:
```bash
   git clone https://github.com/yourusername/route-safety-prediction.git
cd route-safety-prediction
```
2. Run the Jupyter Notebook:
```bash
jupyter notebook
```
3. Execute the cells in the provided Jupyter Notebook files to preprocess the data, train the models, and visualize the results.

## Dataset
The dataset large_routes_features.csv is generated randomly and includes the following features:

- Latitude
- Longitude
- Crime Frequency
- Crime Severity
- Street Lighting
- Pedestrian Traffic
- CCTV Presence
- Police Proximity
- Public Transport Proximity
- Sidewalk Condition

The dataset is generated using a custom Python script, which creates 1,000 rows of random data within specified geographic boundaries.

## Models

The following machine learning models are implemented:

1. Random Forest Classifier: A robust ensemble learning method used for classification tasks.
2. Feedforward Neural Network: A multi-layered neural network that classifies routes into safety levels.

## Results

The accuracy and performance of each model are evaluated using accuracy scores and classification reports. After training, the models can predict safety levels for new routes based on their features.




# lady_guard


This repository contains a machine learning project aimed at predicting the safety levels of various routes based on several geographical and infrastructural features. The project utilizes both Random Forest and Neural Network models to classify routes into three safety levels: Safe, Medium, and Dangerous.

## Project Overview
Women and vulnerable groups face heightened safety risks while walking at night, particularly in poorly lit or unfamiliar areas. Current navigation tools do not prioritize personal safety, often overlooking crucial factors like crime rates, street lighting, and public transport access. This project, Safe Route Suggestor, is an AI-powered navigation system that suggests the safest possible routes by analyzing various factors like crime statistics, lighting quality, police proximity, and more.

This tool is designed to give users peace of mind while walking at night by offering multiple route options ranked based on safety scores, enabling them to choose the best path for a safer journey.

## Problem Statement

Current mapping and navigation tools focus primarily on efficiency (distance and time) but neglect safety factors that are vital for vulnerable groups walking at night. This project aims to fill that gap by developing a system that suggests routes based on personal safety rather than just convenience.

## Features

The Safe Route Suggestor leverages real-time data and machine learning to offer safety-centric routes. Some of the key features include:

- Crime Data Integration: Routes avoid areas with high crime frequency or severity.
- Street Lighting Data: Path suggestions are ranked higher for well-lit streets.
- Police and CCTV Proximity: Areas close to police stations or under CCTV surveillance are preferred.
- Public Transport Access: Routes are ranked higher when they are near public transport hubs.
- Multiple Routes and Ranking: The tool suggests 3-4 alternative routes and ranks them based on safety features.
  
## Tech Stack

The project is built using the following tools and libraries:

- Python: Main programming language for data processing and model development.
- Folium: For map visualization and displaying routes.
- OSRM (Open Source Routing Machine): For routing and obtaining multiple routes between two locations.
- Pandas: For data manipulation and cleaning.
- Scikit-learn: For machine learning (Random Forest, etc.) used in evaluating route safety.
- Keras/TensorFlow: For building and training deep learning models that predict route safety.
- Geopy: For calculating distances and geographical data.
- Requests: For handling API calls to OSRM or similar routing services.

## Dataset

The dataset used for training and evaluation consists of both real and simulated data, which includes the following features for each route:

- Latitude / Longitude: GPS coordinates for each location.
- Crime Type: The type of crime frequently reported in that area.
- Crime Frequency (per month): Number of reported incidents per month.
- Crime Severity: Severity of the crime on a scale of 1 to 10.
- Street Lighting: Quality of lighting along the street (Good/Fair/Poor).
- Pedestrian Traffic: Level of foot traffic (Low/Medium/High).
- CCTV Presence: Whether the area is under CCTV surveillance.
- Police Proximity: Distance to the nearest police station.
- Public Transport Proximity: Distance to the nearest bus stop or train station.
- Sidewalk Condition: The condition of sidewalks along the route (Good/Fair/Poor).

The dataset was either gathered from open data portals (city crime data, street lighting data) or simulated based on known statistics.

## Model

The system uses two types of models:

1. Random Forest Classifier: Used to predict the safety level of a route based on the features in the dataset. It provides a safety score that ranks the routes.
2. Neural Network (Optional): A deep learning model that can also predict safety scores based on a more complex feature set. This is useful for analyzing larger datasets or learning more intricate patterns in the data.
The model takes into account various safety features (crime frequency, street lighting, police presence, etc.) to score each route and suggest the safest one.

## Training and Evaluation

The dataset was split into training and testing sets, with the Random Forest Classifier being trained to classify safety levels (`Safe`, `Medium`, `Dangerous`). After training, the model is evaluated on the test set to ensure accuracy and performance.

## Installation

### Prerequisites

Make sure you have the following installed:

- Python 3.x
- Pip (Python package manager)

### Required Libraries
You can install the required libraries using the following command:

```bash
pip install folium requests pandas scikit-learn tensorflow geopy
```

### Cloning the Repository
Clone this repository to your local machine:

```bash
git clone https://github.com/yourusername/lady_guard.git
```

### Running the Project

1. Navigate to the project directory:
```bash
cd lady_guard
```

2. Open the Jupyter Notebook or run the script:
  
- Using Jupyter Notebook: Launch `safe_route_suggestor.ipynb` to interact with the project.
- Python Script: Run the main script that suggests routes:
  ```bash
  python safe_route_suggestor.py
  ```
3. Enter the start and destination coordinates when prompted. The tool will suggest multiple routes, ranked by safety.
   
## Usage
1. Input Start and Destination: Enter the latitude and longitude for the start and end points of your journey.
2. View Routes: The tool will suggest 3-4 alternative routes based on safety factors.
3. Ranked Output: The safest route is highlighted on the map, along with the reasons (low crime rates, good lighting, proximity to public services).
4. Custom Dataset: You can use your own dataset with safety-related features or integrate it into existing mapping services.

## Future Work
The project can be further expanded with the following features:

- Real-time Data Integration: Incorporate live crime data feeds for more dynamic routing.
- User Feedback: Allow users to rate routes for safety and update the model accordingly.
- Weather Conditions: Factor in weather conditions when suggesting routes.
- Integration with Navigation Apps: Create an API to integrate with apps like Google Maps or Apple Maps.

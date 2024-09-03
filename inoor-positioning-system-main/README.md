Indoor Positioning System Using Beacons and Machine Learning
Introduction
An Indoor Positioning System (IPS) is crucial for applications like navigation within buildings where GPS signals are weak or unavailable. In this project, we developed an IPS that leverages machine learning algorithms and beacons to accurately determine the position of a user or object inside a building.

Components
Beacons (CC2540)
Description: Beacons are wireless devices that use Bluetooth Low Energy (BLE) to broadcast signals to nearby devices.
Function: These signals can be picked up by smartphones to estimate proximity.
Machine Learning Algorithms
We utilized machine learning techniques to analyze beacon signal data:

K-Nearest Neighbors (K-NN)
Random Forest
How It Works
1. Signal Collection (Data Collection)
Setup: Beacons are placed at known locations within a building.
Example Locations: Near the entrance of each store, in the food court, near exits, and key areas like restrooms.
Data Collection: A device (such as a smartphone) collects the strength of beacon signals, also known as the Received Signal Strength Indicator (RSSI).
2. Data Preprocessing
Real-Time Data: As a user moves through the building, the smartphone continuously collects RSSI values from nearby beacons.
Example: If the app receives strong signals from Beacon A but weak signals from Beacon B, the model might predict that the user is near Store X.
3. Position Estimation
Model Training: Machine learning models are trained using collected RSSI data to learn the relationship between RSSI patterns and specific locations.
Real-Time Processing: The trained models estimate the user’s location based on the RSSI values collected in real-time.
Summary
Beacons emit signals, and your device collects RSSI values.
Machine Learning Models are trained on this data to understand the relationship between RSSI patterns and locations.
Real-Time Processing uses these models to estimate your location based on RSSI values as you move around.

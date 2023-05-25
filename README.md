# Anomaly Detection across Multiple Farms through Remote Sensing
 This is a project under the course Agriculture Cyber Physical Systems (CS546) taken in IIT Ropar (Mar 2023 to May 2023). 

### Abstract
An anomaly across multiple farms can be defined as a farm whose growth is not the same as its neighbouring farms, with nearby sowing dates. Anomaly detection across multiple farms can help detect early signs of crop diseases, enabling corrective actions before the disease spreads leading to improved crop yields. Remote sensing technologies, such as satellites and drones, can capture images and data on crops and the surrounding environment from a distance, providing farmers with real-time information on crop growth. Farmers can achieve better crop yields, increased profits, and more sustainable agriculture by making more informed decisions based on anomaly detection through satellite images. A clustering algorithm, such as DBSCAN, can detect anomalies. After proper hyper-parameter tuning, DBSCAN was able to detect the anomalous NDVI value for the respective crop age. Our model first takes input from user the satellite image of current farm that user wants to analyse, we then calculate NDVI of that farm. Now using Wheat_farms_NDVI_data.csv which has data about NDVI values of over 13 farms is used to train DBSCAN. Here we take into consideration the day as age. Day 0 is the day on which sowing was done. Now we do plotting like heat map and others to know the patterns and outliers. We then take from users the input: NDVI value and Age of farms and our output tells which farm is anomalous and which is not. This decsison is done keeping in account the fluctuation in NDVI can be from 0.1-0.3.  We also have trained ARIMA model just to view future prospects of using for prediction.

### How to Run the Project:
Firstly, download the zip file and extract it. Open the code in collab/jupyter and upload all files.

1.	Include the .tif and .xml file which are satellite image data taken from Planet.com
2.	Extract the NIR and RED values and caculate the NDVI of the farm.
3.	Include the Wheat_farms_NDVI_data.csv which contains NDVI values corresponding to dates.
4.	Data Analysis is shown using appropriate graphs and heatmaps.
5.	DBSCAN algorithm is used for anomaly detection.
6.	Min-max scaling is used for normalisation.
7.	Perform the clustering, which results in 3 clusters.
8.	For testing, take input of 5 farms: NDVI value of that day, sowing date and current data & predict the anomalies.
9.	In the end we have displayed ARIMA and Decision tree models to study their accuracies and compare results with DBSCAN.

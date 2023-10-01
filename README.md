# Terrain_Identification_from_Time_Series_Data
Machine learning project using Python, TensorFlow and Keras

# Background
Humans naturally develop walking capability that is energy efficient, stable, environment adaptive, and robust. Lower limb amputations, unfortunately, disrupt this ability; individuals with lower limb amputations usually depend on prosthetic devices to restore the basic walking function. Lower-limb robotic prosthetics can benefit from context awareness to provide enhanced comfort and safety to the amputee. In this work, we aim to develop a terrain identification system based on inertial measurement units IMU streams collected from the lower limb. The system for a prosthetic leg uses visual and inertial sensors though, but we are willing to observe if terrain identification without the visual data is viable. With such information, the control of a robotized prosthetic leg can be adapted to changes in its surrounding.

# [Data Set] Lower Limb IMU


![Screenshot 2023-10-01 164336](https://github.com/dhirdhir1997/Terrain_Identification_from_Time_Series_Data/assets/119910232/fbb0ed00-6b1b-4580-b88b-2d888dd15f9e)

 Note: Not all terrains in the above images have been annotated and the annotations are done by hand for demonstration purposes.

Data will consist of at several sessions from 6 different subjects including IMU data from a sensor on the leg of a participant, and the labels come from annotations of terrain type from a synchronized data stream. We only make use of the IMU data for this project. This work is inspired by this research project: https://research.ece.ncsu.edu/aros/paper-tase2020-lowerlimb/ 

# [Task] Types of terrains

This is a classification task to find different terrains from time series data. The idea is to train a neural network using given data to classify which terrain an unknown data represents. We will use F1 score as the evaluation metric for this project.

# Data files info

Here is a brief description of the data:

  - "_x" files contain the xyz accelerometers and xyz gyroscope measurements from the lower limb.
  - "_x_time" files contain the time stamps for the accelerometer and gyroscope measurements. The units are in seconds and the sampling rate is 40 Hz.
  - "_y" files contain the labels. (0) indicates standing or walking in solid ground, (1) indicates going down the stairs, (2) indicates going up the stairs, and (3) indicates walking on grass.
  - "_y_time" files contain the time stamps for the labels. The units are in seconds and the sampling rates is 10 Hz.

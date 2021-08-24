This repo is for analyzing accelerometer readings , to understand the Fan's normal operation Vs an operation with an anomaly.  
The data is obtained from https://github.com/ShawnHymel/tinyml-example-anomaly-detection.   
In the videos and articles , Shawn has explained how with a set up of  an MPU and an accelerometer attached on the Fan's motor, the motor's vibration data can be collected.    
Once collected , the data is analysed, and models are created for inferencing the data. i.e we learn patterns of the data. We can use simple statistics such as Mahalanobis distance or use Deep learning to map the data.  After selecting the model based on the one which gives the best model metrics, it is then deployed on MPU using tensorflowlite.    
Once anomaly detection model is running on the MPU, the new accelerometer readings are input to the model and based on the predicted value i.e the new mahalanobis distance or the auto encoder prediction's metric such as the mean square error between the actual values and the predicted values, we can identify if the reading is well with in the normal values or is outside as an anomaly.  
I have followed Shawn's approach to creating the models.  
Other methods using PyOD can be tried and tested for better accuracy.  
Also in the videos, Shawn has mentioned that with a change in the setting/ position  of the MPU + Accelerometer, the model needs to be retrained for baseline operation and anomaly detection. Is there a way we to overcome this requirement , other than gathering large number of readings at different settings ??   

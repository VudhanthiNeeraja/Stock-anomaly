# Stock-anomaly
### Anomalies / Outliners:
Anomalies or outliers are individuals that behave in an unexpected way or feature abnormal properties. The problem of identifying these data points or patterns is referred to as outlier/anomaly detection. The significance of anomaly detection lies in actionable information that they provide in different domains such as anomalous traffic patterns in computer networks which may represent intrusion, anomalous MRI images which may indicate the presence of malignant tumours, anomalies in credit card transaction data which may indicate credit card or identity theft, or anomalies in stock markets which may indicate market manipulation.

### Anomalous traffic patterns in a Network.

![image](https://user-images.githubusercontent.com/63281063/151808306-0b5e17b5-a655-4533-bc91-0f82d69bdb89.png)

### Anomalous MRI image.
![image](https://user-images.githubusercontent.com/63281063/151808940-b5d0daed-e203-4292-b746-d75c71dd36f4.png)

### Anomalous Stock.

![image](https://user-images.githubusercontent.com/63281063/151809228-8bd15cf6-d045-4c7c-be99-abd96d78580e.png)

### Time-Series Analysis:
Time series analysis is a specific way of analyzing a sequence of data points collected over an interval of time. In time series analysis, analysts record data points at consistent intervals over a set period of time rather than just recording the data points intermittently or randomly. However, this type of analysis is not merely the act of collecting data over time. What sets time series data apart from other data is that the analysis can show how variables change over time. In other words, time is a crucial variable because it shows how the data adjusts over the course of the data points as well as the final results. It provides an additional source of information and a set order of dependencies between the data. 

Time series analysis typically requires a large number of data points to ensure consistency and reliability. An extensive data set ensures you have a representative sample size and that analysis can cut through noisy data. It also ensures that any trends or patterns discovered are not outliers and can account for seasonal variance. Additionally, time series data can be used for forecasting—predicting future data based on historical data.

## Applying Time Series on Stock:

## ANOMALY DETECTOR: 

The anomaly detector has the following characteristics which play a crucial role in our project.

### 1. Powerful inference engine: 

It assesses our time-series dataset and automatically selects the right anomaly detection algorithm to maximize accuracy for our scenario.

### 2. Automatic detection: 

It eliminates the need for labeled training data to help us save time and stay focused on fixing problems as soon as they surface.

### 3. Customizable settings 

Let's us fine-tune sensitivity to potential anomalies based on the risk profile of our business.

### Detection of the anomalies in the stock using anomaly detector is shown in the below figure

![image](https://user-images.githubusercontent.com/63281063/151932040-08dcd606-0f29-484a-bf7b-06d373fa6150.png)

### USE OF AZURE ANOMALY DETECTOR IN OUR CODE: 

Anomaly Detector ingests time-series data of all types and selects the best anomaly detection algorithm for the data to ensure high accuracy. 

Detect spikes, dips, deviations from cyclic patterns, and trend changes through univariate API's in our project code.

To start of with our project we firstly have to create and deploy our AZURE SERVICE i.e the Anomaly Detector.

## CREATING AND DEPLOYING AZURE SERVICES (ANOMALY DETECTOR):

Step 1: Visit the Microsoft AZURE website and sign up.

Step 2: After signing up you should find the below page loaded.

![image](https://user-images.githubusercontent.com/63281063/151813635-56883f8f-80fb-4dc9-a79f-70a57c49f5dc.png)

Step 3: Click on the search area and search for ANOMALY DETECTORS and select it.

![image](https://user-images.githubusercontent.com/63281063/151813846-ed895be9-8e85-4ced-b7e1-d727d6a2e837.png)

Step 4: After selecting Anomaly Detectors you should find the below page loaded.

![image](https://user-images.githubusercontent.com/63281063/151814140-ef7154fa-ff4a-452b-b38e-37dffd4f4164.png)

Step 5: Now click on create and create and deploy the ANOMALY DETECTOR. After filing all the details click on REVIEW+CREATE.

![image](https://user-images.githubusercontent.com/63281063/151814770-bfa7aa0f-0cbe-47d7-8d34-eea0dcac005d.png)

Step 6: After deploying we can find the below page loaded with the anomaly detector loaded in the overview.

![image](https://user-images.githubusercontent.com/63281063/151815206-3a054895-5c93-4392-889e-654e6a6f3854.png)

Step 7: Click on the created ANOMALY DETECTOR and we can find the below page loaded. We can find the necessary "END POINT" and "API KEYS" (in manage keys).

![image](https://user-images.githubusercontent.com/63281063/151815392-ea5dbe9b-acc4-43a5-94d7-fe7a9d27663e.png)

![image](https://user-images.githubusercontent.com/63281063/151815666-d21bdf8a-9b12-4732-ad94-a9bfe5ff2f74.png)

Thus the AZURE SERVICE is created and deployed successfully.

## INTEGRATING THE PYTHON CODE AND ANOMALY DETECTOR FOR STOCK ANOMALY DETECTION:

Step 1: Copy the API Key and the Endpoint from the ANOMALY DETECTOR that has been created and create the variables such as subscription_key and endpoint to use them in the code and to use these for integrating the detector to the python code.

![image](https://user-images.githubusercontent.com/63281063/151817335-d4aa5e3d-55e8-430a-960a-bcd6cfb75d5e.png)

Step 2: Write the code for the "detect" and the "build_figure" function which uses the API Key and the endpoint to detect the enomalies (uses detect function) and plots the graph as output indicating the boundaries, expected values, values and the anomalies predicted.

![image](https://user-images.githubusercontent.com/63281063/151817448-a9ccbd5b-e956-49fe-ad0b-da7393fa7480.png)

### STOCK PLOT OF THE NON-ANOMALOUS DATA:

![image](https://user-images.githubusercontent.com/63281063/151818405-7c841cec-fb24-45e4-927d-32479647f597.png)

### STOCK PLOT OF THE ANOMALOUS DATA IDENTIFIED BY THE ANOMALY DETECTOR INTEGRATED IN THE PYTHON CODE:

![image](https://user-images.githubusercontent.com/63281063/151818660-41127acd-c34d-4583-be19-18c96ad5b728.png)
The above figure shows the anomaly detected (indicated in red circles).

Thus, the anomalies are detected in the stock data using the AZURE ANOMALY DETECTOR integrated in the python code using the time-series analysis.

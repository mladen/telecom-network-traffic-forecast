# PROJECT: Network Traffic Forecast

## **Project description**

**Objective**: Predict the network traffic load for different times of day or different days of the week.
**Tech Stack**: Python, FastAPI, TensorFlow/Keras (for LSTM models), Pandas, Jupyter Notebook/Lab.
**Steps**:

- Analyze historical network traffic data.
- Preprocess the data into a time-series format.
- Implement an LSTM model, a popular model for time series predictions.
- Validate the model against a test set and visualize the results.

## **Project details**

Let's consider a hypothetical example of historical network traffic data for a telecom operator over several days.

### **Data Structure**:

| Date       | Hour | Data Packets (in millions) | Bandwidth Usage (in Gbps) | Number of Active Users |
| ---------- | ---- | -------------------------- | ------------------------- | ---------------------- |
| 2023-01-01 | 00   | 1.2                        | 3.5                       | 50000                  |
| 2023-01-01 | 01   | 0.8                        | 2.1                       | 30000                  |
| 2023-01-01 | 02   | 0.5                        | 1.4                       | 20000                  |
| ...        | ...  | ...                        | ...                       | ...                    |
| 2023-01-01 | 23   | 1.5                        | 3.8                       | 52000                  |
| 2023-01-02 | 00   | 1.3                        | 3.6                       | 51000                  |
| ...        | ...  | ...                        | ...                       | ...                    |
| 2023-01-31 | 23   | 1.7                        | 4.2                       | 54000                  |

### **Explanation**:

- **Date**: Represents the date for the data entry. Here, it's daily data for January 2023.
- **Hour**: Since we're considering hourly data, this column indicates the hour for which the data is relevant (using a 24-hour format).
- **Data Packets (in millions)**: Indicates the number of data packets transmitted during that hour. A data packet is a unit of data transmitted over the internet. Higher data packets usually imply heavy network usage.
- **Bandwidth Usage (in Gbps)**: This column provides a more direct measure of network usage. It signifies the amount of data transmitted per second during that hour. If the bandwidth usage is approaching the network's capacity, it can lead to congestion and slower internet speeds for users.
- **Number of Active Users**: Represents how many users were active on the network during that hour. This can be a crucial metric, especially for telecom operators, as they need to ensure consistent service even during peak usage times.

### **Data Source**:

Such data typically comes from network monitoring tools and software used by telecom operators to oversee their infrastructure. It's essential for them to continuously track these metrics to ensure optimal performance, detect anomalies, and plan future expansions or upgrades.

For a project, if you don't have access to real data, you can consider generating synthetic time-series data (with realistic patterns) or search for related datasets online on platforms like Kaggle (I see there are several ) or UCI Machine Learning Repository.

# EV Battery Adaptive Test Unit

<p align="center">
  <img src="images/project_banner.png" alt="EV Battery Adaptive Test Unit" width="100%" />
</p>

<h3 align="center"><i>Efficiently test, monitor, and predict the health of EV Lithium-ion batteries.</i></h3>

---

## 💡 Overview

This project proposes a multicell adaptive testing approach for Lithium-ion batteries in Electric Vehicles (EVs) to overcome the limitations of traditional single-cell testing, which is time-consuming and lacks scalability. Our system concurrently estimates the State of Charge (SOC) and State of Health (SOH) of multiple battery cells in parallel, significantly reducing testing time and improving efficiency. It integrates a dual filter concept to select high-quality cells for battery packs and employs a custom Temporal Convolutional Network (TCN) model for accurate SOC/SOH estimation and predictive temperature forecasting. This system aims to enhance battery testing productivity and ensure higher accuracy in estimations, contributing to more reliable and efficient EV batteries.

---

## 🚀 Features

- ⚡ **Multicell Parallel Testing:** Concurrently estimates SOC and SOH for multiple battery cells, reducing testing time and improving efficiency.
- 🎯 **Accurate State Estimation:** Uses adaptive filter-based estimators like Extended Kalman Filters (EKF) and Unscented Kalman Filters (UKF) for precise SOC and SOH estimations.
- 🌡️ **Predictive Temperature Forecasting:** Employs a custom Temporal Convolutional Network (TCN) model to forecast battery temperature over three days.
- 📊 **Real-time Monitoring & Visualization:** Provides a Python-based dashboard for real-time monitoring of battery voltage levels, SOC, and SOH over time.
- ⚙️ **Hardware Integration:** Connects voltage sensors to an ESP32 microcontroller for real-time data acquisition and processing.
- 🔒 **Quality Control:** Incorporates a dual filter concept to categorize cells based on performance, ensuring only high-quality cells are selected.

---

## 📂 Dataset Description

The dataset used for the **EV Battery Adaptive Test Unit** project is generated from controlled experiments on multiple Lithium-ion battery cells (ICR-18650-2500mAh). The data includes:

- **Voltage measurements** from multiple cells captured using voltage sensors connected to an ESP32 microcontroller.
- **Current values** recorded to observe charge and discharge rates.
- **State of Charge (SOC)** and **State of Health (SOH)** values estimated in real-time using Extended Kalman Filter (EKF) and Unscented Kalman Filter (UKF) algorithms.
- **Ambient and battery temperature** measurements used for temperature forecasting with the Temporal Convolutional Network (TCN) model.

### Key Attributes:

| Attribute    | Description                                  |
|--------------|----------------------------------------------|
| Voltage      | Real-time voltage readings per battery cell |
| Current      | Charge/discharge current values              |
| SOC          | Estimated State of Charge (%)                 |
| SOH          | Estimated State of Health (%)                 |
| Temperature  | Battery and ambient temperatures over time  |
| Time         | Timestamp for each measurement                |

### Data Collection Setup:

- **Hardware:** ESP32 WROOM microcontroller, voltage sensors, temperature sensors, Lithium-ion battery cells.
- **Sampling Rate:** Voltage and current data recorded at regular intervals (e.g., every 1 second).
- **Filtering:** EKF and UKF applied onboard for SOC and SOH estimations.
- **Model Inputs:** Sensor readings combined with historical data used to train the TCN model for accurate temperature forecasting.

This dataset allows robust evaluation of battery health and performance under varying load and environmental conditions, forming the basis for predictive maintenance and efficient battery pack management in Electric Vehicles.

---

## 🛠️ Tech Stack

- **Hardware:** ESP WROOM 32 Microcontroller, Voltage Sensors, Lithium-Ion Batteries (ICR-18650-2500mAh)
- **Programming Language:** Python
- **Web Interface:** Streamlit
- **Machine Learning:** scikit-learn, TensorFlow (for TCN model)
- **Numerical Operations:** NumPy, pandas

---

## Report 

The article about the project is provided 
📄 [Article (PDF)](EvbatteryPaper.pdf)

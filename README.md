# Human-Activity-Recognition-Step-Counting-using-Machine-Learning
This project uses accelerometer data to recognize human activities and estimate fitness metrics. It applies signal processing and machine learning to classify activities, count steps, and calculate calories, providing user-level insights from raw sensor data.

## FUNCTIONALITIES

### ACTIVITY RECOGNITION

The system classifies human activities such as Walking, Jogging, Upstairs, Downstairs, Sitting, and Standing using a trained Random Forest model. It processes accelerometer signals to identify patterns associated with each activity.

---

### STEP COUNTING

Step count is estimated using peak detection on filtered acceleration signals. Each detected peak corresponds to a step, enabling approximate tracking of user movement.

---

### SIGNAL PROCESSING

Raw accelerometer data is processed using:
- Magnitude calculation (combining X, Y, Z axes)
- Butterworth low-pass filtering for noise reduction

This improves the quality of the signal before analysis.

---

### WINDOWING & FEATURE GENERATION

The continuous sensor data is divided into fixed-size overlapping windows. For each window, statistical features such as mean and standard deviation are computed to capture activity patterns.

---

### MODEL TRAINING

A Random Forest classifier is used to train the model on extracted features. The dataset is split into training and testing sets to evaluate performance.

---

### MODEL EVALUATION

The system evaluates performance using:
- Accuracy
- Precision
- Recall
- F1 Score
- Confusion Matrix visualization

---

### USER-LEVEL ANALYSIS

The application provides:
- Total step count per user
- Estimated calories burned
- Identification of most active user
- Basic activity-based suggestions

---

## DATASET

The project uses the **WISDM (Wireless Sensor Data Mining) Dataset**, which contains labeled accelerometer data collected from multiple users performing daily activities.

Dataset Source:  
https://www.cis.fordham.edu/wisdm/dataset.php

Note: The dataset is not included in this repository due to its large size. Please download it from the official source.

---

## NOTE

- The system uses Butterworth filtering to reduce noise in sensor data.
- Step counting is based on peak detection and provides approximate results.
- The model is trained using a Random Forest classifier for handling non-linear patterns.
- Input data must follow the format:
  `[user],[activity],[timestamp],[x],[y],[z];`
- Minimal preprocessing assumptions are made; ensure correct dataset format.

---

## LIMITATIONS

- Step count and calorie estimation are approximate
- Model accuracy depends on data quality and parameter tuning
- Not designed for real-time deployment
- Limited input validation

---

## FUTURE IMPROVEMENTS

- Integration with real-time mobile sensor data  
- Personalized fitness tracking  
- Advanced deep learning models for time-series data  
- Deployment as a web or mobile application  

---

## LICENSE

This project is intended for educational purposes. You are free to use, modify, and distribute it under an appropriate open-source license (e.g., MIT License).

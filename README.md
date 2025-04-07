<h1 align="center">Grammar Scoring Engine for Voice Samples</h1>

<div align= "center">
  <h4>Evaluate spoken grammar using machine learning and voice features</h4><br>
</div>

# Overview
The Grammar Scoring Engine for Voice Samples project focuses on evaluating the grammatical correctness of spoken sentences using machine learning techniques. The goal is to build a robust and automated system that can analyze voice inputs and assign grammar scores, helping improve spoken language proficiency—especially in educational or language learning settings.
This engine leverages features extracted from voice samples—such as acoustic signals, speech-to-text conversions, and linguistic markers—to evaluate grammar quality. The application is particularly useful for learners, educators, and assessment platforms aiming to automate spoken grammar evaluation.
# 📁Dataset Description
The dataset consists of audio files and corresponding CSV metadata files.<br>
•🔊 Audio Files

     Format: .wav

     Each file contains a short speech sample.

•📄 CSV Files

    train.csv:
    
    Contains file names and corresponding grammar score labels for training.

    test.csv:
    
    Contains only file names for testing. Labels are not included.
    
📊 Data Split

  Training Samples: 444

  Testing Samples: 195
# Some Screenshots

• **A person who smoke and have BMI above 30 tends to have a higher medical cost** <br>

![image](Images/photo_2025-02-27_10-26-00.jpg)

• **A person who smoke and have BMI above 30 tends to have a higher medical cost** <br>

![image](Images/photo_2025-02-27_10-26-00.jpg)

• **Correlation Heatmap of Features and Target Variable (Charges)** <br>

![image](Images/photo_2025-02-27_11-43-46.jpg)


# Feature Importance

• **Importance of individual features** <br>
![image](Images/photo_2025-02-27_11-10-19.jpg)

• **Most important features for predicting of charges** <br>
![image](Images/photo_2025-02-27_11-12-28.jpg)


# Model Evaluation

| Score | LinearRegression | Support Vector Machine | RandomForest | Gradient Boost| XGBoost|
| ----------- | ----------- | ----------- | ----------- | ----------- | ----------- |
| Train Accuracy | 0.729 | -0.105 | 0.97 | 0.868 |0.870 |
| Test Accuracy | 0.806 | -0.134 | 0.882 | 0.901 | 0.904 |
| CV Score | 0.747 | 0.103 | 0.836 | 0.860 | 0.860 |

# Conclusion
Model gave 90% accuracy for Medical Insurance Amount Prediction using XGBoost. This project demonstrates the effectiveness of machine learning, particularly XGBoost, in accurately predicting medical insurance costs based on key factors. It aims to enhance cost transparency and planning, benefiting both insurers and customers.

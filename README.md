<h1 align="center">Grammar Scoring Engine for Voice Samples</h1>

<div align= "center">
  <h4>Evaluate spoken grammar using machine learning and voice features</h4><br>
</div>

# Overview
The Grammar Scoring Engine for Voice Samples project focuses on evaluating the grammatical correctness of spoken sentences using machine learning techniques. The goal is to build a robust and automated system that can analyze voice inputs and assign grammar scores, helping improve spoken language proficiency—especially in educational or language learning settings.
This engine leverages features extracted from voice samples—such as acoustic signals, speech-to-text conversions, and linguistic markers—to evaluate grammar quality. The application is particularly useful for learners, educators, and assessment platforms aiming to automate spoken grammar evaluation.

# 📁 File Contents

  • shl.ipynb – Main notebook containing:
  
  • Data import and exploration
  
  • Preprocessing steps
  
  • Model training and evaluation
  
  • Visualizations and result interpretations
  
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


# 🔍 1. Data Import and Exploration
  • Libraries Imported:
    
  pandas, whisper (OpenAI), librosa, sentence-transformers, scikit-learn, xgboost, lightgbm, matplotlib, tqdm.

  • Whisper Model:
    
  The small variant of OpenAI's Whisper is used for automatic audio transcription

# 🧹 2. Preprocessing Steps
  • Audio Transcription:
  
  Each audio file is transcribed to text using Whisper:
  
  Transcriptions are stored as a new column: train_df["transcript"]

  • Text Embedding:
  
  Transcribed texts are converted to numerical vectors using Sentence-BERT

# 🤖 3. Model Training and Evaluation
  • Target Variable:
  
    y_train = train_df["label"].values (Likely regression, not classification)
  
  • Models Used:
  
    Ridge Regression
  
    XGBoost Regressor
  
    LightGBM Regressor
  
    Ensemble Method:
    
  A VotingRegressor combines all three
    
 • Evaluation Metric:
 
  Pearson correlation coefficient is used to evaluate the predictions from cross-validation
  
# 📊 4. Visualizations and Result Interpretations
• Scatter Plot:

  A scatter plot is generated to compare predicted vs actual labels
  ![image](images/imagejpg)
  
• Interpretation:

  High correlation indicates model effectiveness in capturing the target variable from transcribed speech.

# 📁 Output Artifacts

Transcribed text for each audio file

Sentence embeddings

Trained ensemble model (in memory)

Pearson correlation score

Diagnostic plots

# Conclusion
Model gave 90% accuracy for Medical Insurance Amount Prediction using XGBoost. This project demonstrates the effectiveness of machine learning, particularly XGBoost, in accurately predicting medical insurance costs based on key factors. It aims to enhance cost transparency and planning, benefiting both insurers and customers.

#  Tweet Emotion Detection
## Overview

The **Tweet Emotion Detection Model** is a Python-based application leveraging **Natural Language Processing (NLP)** techniques to classify the emotions conveyed in tweets. This tool aims to analyze tweet content and detect emotions such as **joy**, **sadness**, **fear**, **neutral**, **anger**, and **shame**. It uses a trained machine learning model and offers a user-friendly interface powered by **Streamlit**.

##  Features
- **Fetch tweets** directly from a given Twitter/X URL.
- **Predict emotions** like `happy`, `sad`, `fear`, `anger`, `surprise`, `neutral`, `disgust`, and `shame`.
- **Emoji mapping** for better visual interpretation.
- **Probability chart** using Altair for prediction confidence.
- Simple **web UI** powered by Streamlit.

##  Tech Stack
- **Python 3**
- [Streamlit](https://streamlit.io/) – Web app framework
- **scikit-learn** – Model training & prediction
- **pandas**, **numpy** – Data processing
- **Altair** – Data visualization
- **joblib** – Model loading
- **Requests** – Fetch tweet content

## Project Structure
├── app.py # Main Streamlit app
├── text_emotion.pkl # Pre-trained ML model
├── tweet_dataset.csv # Dataset used for training
├── Text_Emotion_Detection.ipynb # Notebook for model training
└── README.md # Project documentation

##  Installation & Usage

 **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/tweet-emotion-detection.git
   cd tweet-emotion-detection
   ```

## Dataset Details

The dataset used for training contains text samples labeled with emotions. It underwent several preprocessing steps:
- Removal of stop words, user handles, and special characters using the **Neat Text** library.
- Addition of a column for cleaned text to prepare the data for model training.

## Model Training

The model was trained using Scikit-learn with the following algorithms:
1. **Support Vector Machines (SVM)**: For robust classification by finding optimal decision boundaries.
2. **Random Forest Classifier**: Utilizes an ensemble of decision trees for accurate predictions.
3. **Logistic Regression**: Effective for categorical output prediction.

`The dataset was split:
- **70% Training Set**: Used for model training.
- **30% Testing Set**: Used for evaluating the model's performance.

##Install dependencies
```bash
pip install -r requirements.txt
```
##Run the app
```bash
streamlit run app.py
```
##Open in Browser
```bash
 http://localhost:8501
```
Paste a Tweet/X URL and see the detected emotion.

##Example 
```bash
https://twitter.com/elonmusk/status/123456789
```
##Output:
Emotion: happy 😂
Confidence: 0.92

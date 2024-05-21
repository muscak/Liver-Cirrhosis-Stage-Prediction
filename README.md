# Liver Cirrhosis Stage Prediction 
Prediction of the stage of liver cirrhosis of a patient. 

## Problem Definition

> <img src='static/images/liver.png' width='10%' align="center"> Cirrhosis results from prolonged liver damage, leading to extensive scarring, often due to conditions like hepatitis or chronic alcohol consumption.

In this study we'll tyr to predict the stage of the cirrhosis for a person with the given parameters. Since the number of outcomes are limited, we'll approach this problem as a multi-class classification problem. We'll select and train a machine learning algorithm based on the performance metric which will be deciden in the upcoming section.

To install the required libraries, run the following command:
```bash
pip install -r requirements.txt
```

### How to run it locally

#### Terminal
```bash
uvicorn main:asgi_app --port 10000
```

#### IDE
```bash
Create a python run configuration and choose the main.py file
```

#### Docker
1. Run `docker build -t cirrhosis-prediction .`
2. Run `docker run -p 10000:10000 cirrhosis-prediction`
3. Open your browser and go to `http://localhost:10000/`

#### Online
API: https://cirrhosis-prediction-render.onrender.com//predict_api
```JSON
{
    "N_Days": 1567,
    "Status": "C",
    "Drug": "Placebo",
    "Age": 15373,
    "Ascites": "Y",
    "Hepatomegaly": "N",
    "Spiders": "Y",
    "Bilirubin": 0.3,
    "Cholesterol": 136,
    "Albumin": 3.75,
    "Copper": 15,
    "Alk_Phos": 976,
    "SGOT": 53,
    "Tryglicerides": 78,
    "Platelets": 220,
    "Prothrombin": 10.3
}
```


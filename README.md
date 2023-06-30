# diabetes_api_ml

The objective of the API is to diagnostically predict whether or not a patient has diabetes, based on certain diagnostic measurements included in the dataset. Several constraints were placed on the selection of these instances from a larger database. In particular, all patients here are females at least 21 years old of Pima Indian heritage.

Dataset Citation: https://www.kaggle.com/datasets/uciml/pima-indians-diabetes-database

AVAILABLE AS API IN RAPID API HUB: https://rapidapi.com/satwikvbolar23/api/diabetes-api

Hosted URL: https://diabetes-api-ml-1he0.onrender.com/diabetes_prediction


### IMPLEMENTATION OF API: 

api_implementation.py

import json
import requests

url = 'https://diabetes-api-ml.onrender.com/diabetes_prediction'

input_data_for_model = {
  'pregnancies': 5,
  'Glucose': 166,
  'BloodPressure': 72,
  'SkinThickness': 19,
  'Insulin': 175,
  'BMI': 25.8,
  'DiabetesPedigreeFunction': 0.587,
  'Age': 51
}

input_json = json.dumps(input_data_for_model)

response = requests.post(url, data=input_json)

print(response.text)


### Output:
![image](https://github.com/satwikbolar/diabetes_api_ml/assets/82822150/35775048-92cc-4ca2-abae-a759b6a46639)


# Iris Classifier with BentoML

This project demonstrates how to train, serve, and test a machine learning model using [BentoML](https://bentoml.org/). The model classifies iris flower species using a scikit-learn SVM and is served as an API.

## 📁 Project Structure

BentoML/
├── requirements.txt
├── train.py
├── service.py
└── test.py

bash
Copy
Edit

## 📦 Setup

1. **Create a virtual environment (optional but recommended)**:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
Install dependencies:

bash
Copy
Edit
pip install -r requirements.txt
🧠 Training the Model
Train and save the model using:

bash
Copy
Edit
python train.py
This saves the model to BentoML's local model store.

🚀 Serving the Model
Use BentoML to start the API server:

bash
Copy
Edit
bentoml serve service:svc
The server will start and expose a POST endpoint at:

bash
Copy
Edit
http://localhost:3000/classify
🧪 Testing the Model
You can test the model locally (without starting a server) using:

bash
Copy
Edit
python test.py
This will run a prediction using the latest saved model.

📝 Example API Call
Once the server is running, you can test it with curl or Postman:

bash
Copy
Edit
curl -X POST http://localhost:3000/classify \
  -H "Content-Type: application/json" \
  -d '[[5.9, 3.0, 5.1, 1.8]]'
📌 Notes
Make sure to train the model before serving or testing it.

The model tag (e.g., iris_clf:latest) is used to reference the latest saved version.

You can explore all saved models using:

bash
Copy
Edit
bentoml models list
📚 Requirements
bentoml==1.0.25

scikit-learn

numpy

Install them using:

bash
Copy
Edit
pip install -r requirements.txt
📤 Deployment
You can later containerize and deploy this service using:

bash
Copy
Edit
bentoml containerize service:svc

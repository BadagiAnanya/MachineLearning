# Iris Classifier with BentoML

This project demonstrates how to train, serve, and test a machine learning model using [BentoML](https://bentoml.org/). The model classifies iris flower species using a scikit-learn SVM and is served as an API.

## 📁 Project Structure

```bash
BentoML/
├── requirements.txt
├── train.py
├── service.py
└── test.py
📦 Setup
Create a virtual environment (optional but recommended):

bash
Copy
Edit
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

yaml
Copy
Edit

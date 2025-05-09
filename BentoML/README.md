# Build and Deploy an Iris Classifier with BentoML 🌸

This project demonstrates how to leverage [BentoML](https://bentoml.org/) to build, serve, and test a machine learning model. We'll train a Support Vector Machine (SVM) using scikit-learn to classify different species of iris flowers and then deploy it as a scalable API.

## 📂 Project Layout
**Tree View:**
IrisClassifier/
├── requirements.txt
├── service.py
├── test.py
└── train.py
## 🛠️ Getting Started

1.  **Set up a Virtual Environment (Recommended):**
    Isolate your project dependencies for a cleaner environment.

    ```bash
    python -m venv venv
    source venv/bin/activate   # Linux/macOS
    # venv\Scripts\activate    # Windows
    ```

2.  **Install Dependencies:**
    Ensure you have all the necessary libraries.

    ```bash
    pip install -r requirements.txt
    ```

## 🧠 Train the Iris Model

Execute the training script to build and save your classification model using BentoML's model store.

```bash
python train.py
```
This command trains the SVM model on the Iris dataset and saves it as a BentoML bundle.

##🚀 Serve the Model via API
Deploy your trained model as a REST API with a single BentoML command.
```bash
bentoml serve service:svc
```
Once the server starts, you can send prediction requests to the following endpoint:
```bash
http://localhost:3000/classify
```

##🧪 Test Locally
Verify your model's functionality directly without needing to interact with the live API.
```bash
python test.py
```









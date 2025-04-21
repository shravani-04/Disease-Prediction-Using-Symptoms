🩺 Disease Prediction System using Machine Learning
This project is a web-based disease prediction system that uses machine learning algorithms to predict the most likely disease based on selected symptoms. It supports four symptom inputs and uses three classifiers — Random Forest, Support Vector Machine (SVM), and Naive Bayes — to provide predictions.

🎯 The final disease prediction is made by taking the majority vote (mode) from the three models.

📌 Features
Predicts disease based on 4 selected symptoms

Uses Random Forest, SVM, and Naive Bayes classifiers

Trained on a comprehensive medical dataset

Includes a Flask-powered web interface

Outputs the most likely disease based on user input

Final result based on majority vote from 3 models

🧠 Algorithms Used
Random Forest Classifier
A powerful ensemble learning method based on decision trees. It reduces overfitting and improves accuracy by combining predictions from multiple trees.

Support Vector Machine (SVM)
A supervised learning algorithm that classifies data by finding the optimal separating hyperplane in high-dimensional space.

Gaussian Naive Bayes
A probabilistic classifier based on Bayes’ theorem. Assumes feature independence and is fast and efficient for high-dimensional data.

The final prediction is determined by the mode (most frequent) of the three predictions.

🧾 Dataset
Dataset Source: Training.csv.zip & Testing.csv

Each row contains a list of symptoms with the corresponding disease (prognosis).

The ‘prognosis’ column is label-encoded using sklearn's LabelEncoder.

⚙️ How It Works
User selects 4 symptoms on the web interface.

These symptoms are converted into a binary feature vector.

This input is passed to each model (RF, SVM, NB).

Each model predicts a disease.

The final output is the disease that appears most often among the 3 predictions.

📁 Project Structure
bash
Copy
Edit
├── Training.csv.zip                # Training dataset
├── Testing.csv                    # Testing dataset
├── rf_model.pkl                   # Saved Random Forest model
├── svm_model.pkl                  # Saved SVM model
├── nb_model.pkl                   # Saved Naive Bayes model
├── app.py                         # Flask application file
├── templates/
│   ├── index2.html                # Input form for symptoms
│   └── predict.html               # Result display page
├── static/
│   └── style.css (optional)      # Add if you style your frontend
├── README.md                      # This file
🚀 How to Run the Project
Clone the repository

bash
Copy
Edit
git clone https://github.com/your-username/disease-prediction-ml.git
cd disease-prediction-ml
Install dependencies

bash
Copy
Edit
pip install pandas numpy scikit-learn matplotlib seaborn flask
Run the Flask app

bash
Copy
Edit
python app.py
Open your browser and go to http://127.0.0.1:5000/

🖥️ Web Interface
Symptom input is provided through dropdowns.

After form submission, the web app displays the predicted disease.

Final output is based on model majority vote.

📊 Model Evaluation
Each model was trained on the training data and tested on a separate testing dataset.

Example accuracy:

Random Forest: ~99%

SVM: ~97%

Naive Bayes: ~92%

Combined Model (Voting): ~98–99%

🧠 Sample Prediction
Input: Itching, Skin Rash, Nodal Skin Eruptions
Prediction: Fungal Infection (Example output)


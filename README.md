# 🧠 Employee Churn Prediction using ANN

This project is an end-to-end **Artificial Neural Network (ANN)** application that predicts whether an employee will leave the company or not. It is built using **TensorFlow** for model training and deployed with an interactive **Streamlit** UI. The model is trained on the `Churn_Modelling.csv` dataset and includes encoder pipelines for categorical variables. **TensorBoard** is integrated to analyze model performance.

---

## 📁 Project Structure

```plaintext
├── app.py # Streamlit app to run the prediction
├── model.pkl # Trained ANN model saved using pickle
├── label_encoder_gender.pkl # LabelEncoder for encoding Gender
├── onehot_encoder_geo.pkl # OneHotEncoder for Geography
├── Churn_Modelling.csv # Dataset used for training
├── requirements.txt # Python dependencies
├── notebooks/
│ ├── Experiments.ipynb # Data preprocessing steps
│ └── predictions.ipynb # ANN model training with TensorBoard
```

---

## 🛠️ Tech Stack

- **Frontend:** Streamlit  
- **Backend Model:** TensorFlow (ANN)  
- **Model Monitoring:** TensorBoard  
- **Serialization:** Pickle  
- **Encoders:**
  - `LabelEncoder` for Gender
  - `OneHotEncoder` for Geography

---

## 🧪 Dataset Description

- **File Used:** `Churn_Modelling.csv`
- **Features Include:**
  - Credit Score
  - Geography
  - Gender
  - Age
  - Tenure
  - Balance
  - Number of Products
  - Has Credit Card
  - Is Active Member
  - Estimated Salary
- **Target:** `Exited` (1 - Employee will leave, 0 - Employee stays)

---

## 📊 TensorBoard Integration

During training, **TensorBoard** was used to monitor:

- Accuracy and loss metrics
- Training vs Validation performance
- Graph structure and profiling

To launch TensorBoard (from the `notebooks` folder):

```bash
tensorboard --logdir=logs
```

---

## 🚀 Running the App

### 1. Clone the Repository
```bash
git clone https://github.com/sliitguy/Churn-Prediction-ANN.git
cd employee-churn-ann
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

### 3. Run the Streamlit App
```bash
streamlit run main.py
```

---

## 🧮 Model Workflow
### 1. Preprocessing:
- Encode Gender using LabelEncoder (saved as label_encoder_gender.pkl)
- Encode Geography using OneHotEncoder (saved as onehot_encoder_geo.pkl)

### 2. Model Training:
- Train a deep learning model using TensorFlow's Sequential API
- Use ReLU activation in hiddel layers and Sigmoid in the output layer

### 3. Model Saving:
- Save the trained model using pickle for reuse.

### 4. Deployment
- Load model and encoders in app.py
- Build a user-friendly interface using Streamlit

### 5. User Interaction:
- Allow users to input employee features
- Display prediction along with percentage: Whether the employee is likely to leave








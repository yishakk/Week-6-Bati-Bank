---

# **Project Title:Bati Bank Credit Score**  
_Credit scoring is the term used to describe the process of assigning a quantitative measure to a potential borrower as an estimate of how likely the default will happen in the future. Traditionally, creditors build credit scoring models using statistical techniques to analyze various information of previous borrowers in relation to their loan performance. Afterward, the model can be used to evaluate a potential borrower who applies for a loan by providing the similar information which has been used to build the model. The result is either a score which represents the creditworthiness of an applicant or a prediction of whether an applicant will default in the future._

---

## **Project Overview**  
This project focuses on developing and deploying machine learning models for real-time predictions. The workflow includes data preprocessing, model training, evaluation, and serving the trained models through a REST API for live predictions. 

Key objectives:  
1. Implement machine learning models to solve Credit Score.    
2. Deploy the models using an API for real-time integration.  

---

## **Features**  
- **Data Preprocessing**: Data cleaning, transformation, and Weight of Evidence (WoE) encoding.  
- **Model Training**: Logistic Regression and Random Forest with hyperparameter tuning.  
- **Model Evaluation**: Comprehensive performance metrics and ROC curve visualization.  
- **API Integration**: A REST API built with [Framework, e.g., FastAPI or Flask] for real-time predictions.  

---

## **Repository Structure**  

```
project-root/
│
├── data/
│   ├── raw_data.csv                  # Original dataset
│   ├── rfms_woe_transformed_data.csv # Processed dataset with WoE encoding
│
├── models/
│   ├── logistic_model.pkl            # Saved Logistic Regression model
│   ├── random_forest_model.pkl       # Saved Random Forest model
│
├── notebooks/
│   ├── data_preprocessing.ipynb      # Jupyter notebook for data preprocessing
│   ├── model_training.ipynb          # Jupyter notebook for model training and evaluation
│
├── scripts/
│   ├── train_models.py               # Script for training models
│   ├── serve_api.py                  # API script for model serving
│
├── outputs/
│   ├── model_performance_metrics.csv # Evaluation metrics for trained models
│   ├── model_predictions.csv         # Predictions from the trained models
│
├── README.md                         # Documentation file (you are here!)
```

---

## **Installation Guide**  

1. Clone the repository:
   ```bash
   git clone https://github.com/yishakk/Week-6-Bati-Bank.git
   cd your-repo
   ```

2. Install dependencies:  
   ```bash
   pip install -r requirements.txt
   ```

3. Download or generate datasets and place them in the `data/` directory.

4. Run the model training script:  
   ```bash
   python scripts/train_models.py
   ```

5. Serve the API for predictions:  
   ```bash
   python scripts/serve_api.py
   ```

---

## **Usage**  

### **Training Models**
1. Use `train_models.py` to preprocess data and train machine learning models.  
2. The trained models are saved as `.pkl` files in the `models/` directory.

### **Model Predictions via API**  
1. Run `serve_api.py` to launch the REST API.  
2. Example cURL request for predictions:  
   ```bash
   curl -X POST "http://127.0.0.1:8000/predict" \
   -H "Content-Type: application/json" \
   -d '{"input_data": {"feature1": 1, "feature2": 0, "feature3": 5}}'
   ```

---

## **Project Contributions**  

### **Your Contributions**  
- Designed and implemented machine learning pipelines for preprocessing, training, and evaluation.  
- Conducted hyperparameter tuning to optimize model performance.  
- Developed a REST API for serving real-time predictions using FastAPI.  
- Documented all workflows and scripts for reproducibility.  

### **Acknowledgments**  
- Open-source libraries and frameworks, including [Sklearn, Pandas, Flask, etc.].

---

## **Future Improvements**  
- Add additional models like Gradient Boosting or Neural Networks.  
- Enhance API security and scalability for production use.  
- Extend feature engineering to improve model accuracy.  

---

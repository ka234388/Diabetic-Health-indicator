# Diabetic Health Indicator

## Problem Definition

### Task Definition
The task is to develop a machine learning model to classify individuals' diabetes status based on various health indicators. The three possible outcomes are:
- **Class 0**: No diabetes.
- **Class 1**: Pre-diabetes.
- **Class 2**: Diabetes.

The dataset used is the **BRFSS 2015 diabetes dataset**, containing health metrics such as BMI, age, physical activity, and other medical conditions.

### Motivation
Diabetes is a major global health concern, and early detection can reduce long-term complications. This project aims to provide an automated tool for diabetes risk assessment.

Key motivations:
- **Global Health Impact**: Rising diabetes prevalence demands better detection tools.
- **Automation & Scalability**: Machine learning provides fast and reliable diabetes risk assessment.
- **Data-Driven Insights**: The model will highlight key health factors influencing diabetes, aiding individuals and healthcare practitioners.

### Objective
Develop a machine learning model that accurately classifies an individual’s diabetes status using health indicators, with **accuracy** as the primary evaluation metric.

## Dataset Details

The dataset consists of **253,680 entries and 22 columns**, including:
- **Health condition indicators**: HighBP, HighChol, Stroke, HeartDiseaseorAttack
- **Lifestyle factors**: PhysActivity, Smoker, HvyAlcoholConsump, Fruits, Veggies
- **Healthcare & health status**: AnyHealthcare, NoDocbcCost, GenHlth, MentHlth, PhysHlth, DiffWalk
- **Demographics**: Sex, Age, Education, Income
- **Target variable**: `Diabetes_012` (0: No diabetes, 1: Prediabetes, 2: Diabetes)

# Diabetic Health Indicator

## Multilayer Perceptron (MLP) Model

### Model Architecture
The predictive model is a **Multi-Layer Perceptron (MLP)** implemented using **PyTorch** for multi-class classification of diabetes risk.

- **Input Layer**: 21 health indicators.
- **Hidden Layers**: Four fully connected layers with neuron reduction (512 → 256 → 128 → 64).
- **Dropout Regularization**: 0.3 dropout rate to mitigate overfitting.
- **Output Layer**: Three neurons for multi-class classification (No Diabetes, Pre-Diabetes, Diabetes).

### Loss Function & Optimization
- **Loss Function**: Weighted **Cross-Entropy Loss** to address class imbalance.
- **Optimizer**: **Adam Optimizer** with dynamic learning rate adjustments.
- **Learning Rate Adjustment**: **ReduceLROnPlateau scheduler** reduces learning rate by 0.5 when validation loss plateaus.

## Training Process
- **Epochs**: 150
- **Batch Size**: 64 for balanced memory and efficiency.
- **Training Progress**:
  - **Epoch 1**: Training Loss = **0.7543**, Validation Loss = **0.6858**.
  - **Epoch 20**: Training Loss = **0.4024**, Training Accuracy = **82.6%**, Validation Accuracy = **84.25%**.
  - **Final Epoch**: Training Loss = **0.2051**, Training Accuracy = **91.18%**, Validation Accuracy = **90.28%**.

## Validation & Early Stopping
- **Validation loss and accuracy monitored** to prevent overfitting.
- **Early stopping** implemented to halt training when validation improvements plateau.
- **Final validation loss** stabilized at **0.2373**, indicating **strong generalization**.

## Model Evaluation
### Classification Report
- **Precision**: Measures true positive predictions for each class.
- **Recall**: Measures the ability to identify actual positive instances.
- **F1-Score**: Balances precision and recall across all classes.
- **Overall Accuracy**: **90%**, with macro-average and weighted-average metrics confirming balanced performance.

### Confusion Matrix
- **Strength**: Highest precision and recall for **Class 1 (Pre-Diabetes)**.
- **Challenge**: Slightly higher misclassification rate for **Class 2 (Diabetes)**.
- **Overall**: **90% accuracy**, with balanced performance across precision, recall, and F1-score.

## Visualization
Comprehensive plots were created to illustrate model performance:
1. **Loss vs. Epochs**: Shows the decline in training and validation loss, confirming effective learning.
2. **Accuracy vs. Epochs**: Demonstrates improved training and validation accuracy over time.
3. **Confusion Matrix**: Highlights correct and misclassified predictions for each class.

# Diabetic Health Indicator

## Model Performance
Refer images
### Loss vs. Epochs
Refer images
### Accuracy vs. Epochs
Refer images
### Confusion Matrix
Refer images
### Classification Report MLP
Refer images
---

### How to Use the Model
1. Clone this repository:
   ```sh
   git clone https://github.com/ka234388/Diabetic-Health-indicator.git
   ## Setup and Usage Instructions

### **Requirements**
- This project contains a **Jupyter Notebook (`.ipynb` file)**.
- Ensure that Python is installed with the correct version.
- Install dependencies using:
  ```sh
  pip install -r requirements.txt


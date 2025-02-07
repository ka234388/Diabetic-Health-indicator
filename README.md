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

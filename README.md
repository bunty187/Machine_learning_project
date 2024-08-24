# Scania APS Failure Detection Machine Learning Project

## Project Overview
The **Scania APS (Air Pressure System) Failure Detection** project aims to develop a machine learning model to predict potential failures in the air pressure system of Scania trucks. The air pressure system (APS) generates pressurized air used in various functions in a truck, such as braking and gear changes. Predicting failures in this system is crucial to avoid costly repairs and ensure vehicle safety.

## Problem Statement
The datasets provided contain information on the air pressure system (APS) in trucks. The positive class in the dataset corresponds to component failures specific to the APS system. The negative class represents trucks with failures in components unrelated to the APS system.

The main objective of this project is to **reduce the cost associated with unnecessary repairs and missed detections**. Therefore, the focus is on minimizing false predictions, especially false negatives, since missing a faulty truck (false negative) incurs a much higher cost than an unnecessary check (false positive).

### Cost Implications:
* **Cost 1 (False Positive Cost)**: The cost incurred when an unnecessary check is performed on a truck that is actually not faulty.
    * Cost 1 = 10 units.
* **Cost 2 (False Negative Cost)**: The cost incurred when a faulty truck is missed, which may lead to a breakdown.
    * Cost 2 = 500 units.

The **Total Cost** of the prediction model is calculated as:

Total_cost = (Cost1 × No_Instances_False_Positive) + (Cost2 × No_Instances_False_Negative)

Given the cost disparity, the goal is to **reduce false negatives** (missing a faulty truck), as it is 50 times more costly than a false positive.

## Key Steps in the Project:
1. **Data Extraction**: Extracting data from MongoDB.
2. **Data Validation**: Ensuring data quality and consistency.
3. **Data Transformation**: Preprocessing data for model building.
4. **Model Evaluation**: Developing and evaluating models to minimize false negatives.
5. **Model Deployment**: Deploying the optimal model on AWS for real-time predictions.

### Getting Started
#### Prerequisites
To run this project, you'll need the following:

2.Clone the Repository
```
git clone https://github.com/yourusername/scania_aps_failure_detection.git
cd scania_aps_failure_detection

```

3. Install the Required Libraries
```
pip install -r requirements.txt
```
4. Run the Project
```
python main.py
```


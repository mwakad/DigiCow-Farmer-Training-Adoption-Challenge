# DigiCow-Farmer-Training-Adoption-Challenge

## Aim
To predict which farmers in Kenya are likely to adopt improved practices/ turn evidence-based technologies into action within 4 months after receiving high-quality agricultural training. 

## Problem Statement
Access to high-quality agricultural training is just the first step toward improving productivity of farms. However, understanding which farmers adopt improved practices after training and why is a real challenge.

## Business Understanding
DigiCow supports smallholder farmers through digital tools, extension services, and targetted training programmes. However, like many real-world interventions, adoption rates remain low and uneven. The ability to predict adoption early can enable DigiCow and its partners to prioritise follow-ups, tailor support more effectively, and design stronger extension strategies. 

## Project Pitch
Predict the probability that a farmer will adopt a practice within 120 days of their first training, only using information available at the time of training. So the trained model must output predicted probabilities indicating the likelihood that a farmer will adopt a DigiCow-supported practice within the target time window (120 days of their first training). 

## Datasets
    1) dataset_data_dictionary.csv: A full description of all the features in the dataset.
    2) Train.csv: The data to train and validate the models.
    3) Test.csv: Contains same features as Train.csv except the target variable.
    4) SampleSubmission.csv: Required submission file format. 

## Evaluation Metric
A multi-metric evaluation:
    1. Log Loss (70%): To encourage the model to output probability estimates by penalizing confident but incorrect predictions more heavily.
    2. ROC-AUC (30%): To measure the model’s ability to rank adopters above non-adopters across all possible thresholds to provide a stable assessment of overall ranking since the dataset is imbalanced. 

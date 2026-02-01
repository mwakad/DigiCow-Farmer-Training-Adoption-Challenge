# DigiCow-Farmer-Training-Adoption-Challenge

## Aim
To predict which farmers in Kenya are likely to adopt improved practices/ turn evidence-based technologies into action within 4 months after receiving high-quality agricultural training. 

## Problem Statement
Access to high-quality agricultural training is just the first step toward improving productivity of farms. However, understanding which farmers adopt improved practices after training and why is a real challenge.

## Business Understanding
DigiCow supports smallholder farmers through digital tools, extension services, and targetted training programmes. However, like many real-world interventions, adoption rates remain low and uneven. The ability to predict adoption early can enable DigiCow and its partners to prioritise follow-ups, tailor support more effectively, and design stronger extension strategies. 

## Project Pitch
Predict the probability that a farmer will adopt a practice within, 07, 90, and 120 days of their first training, only using information available at the time of training. So the trained model must output predicted probabilities indicating the likelihood that a farmer will adopt a DigiCow-supported practice within the target time window (7 days of their first training, 90 days of their first training, and 120 days of their first training). 

## Datasets
    1) dataset_data_dictionary.csv: A full description of all the features in the dataset.
    2) Train.csv: The data to train and validate the models.
    3) Test.csv: Contains same features as Train.csv except the target variable.
    4) SampleSubmission.csv: Required submission file format. 

## Primary Features: 
| Feature Index | Feature Name              | Description                                                                 |
|---------------|--------------------------|-----------------------------------------------------------------------------|
| 0             | ID                       | Unique identifier for each farmer entry                                     |
| 1             | gender                   | Gender of the farmer                                                        |
| 2             | age                      | Age category of the farmer                                                  |
| 3             | registration             | Registration method                                                         |
| 4             | belong_to_cooperative    | Whether the farmer belongs to a cooperative (1 = yes, 0 = no)              |
| 5             | county                   | County of residence                                                         |
| 6             | subcounty                | Sub-county of residence                                                     |
| 7             | ward                     | Ward of residence                                                           |
| 8             | trainer                  | Trainer who delivered the training                                          |
| 9             | topics_list              | List of possible training topics                                            |
| 10            | first_trainings_date     | Date of the farmer's first training                                         |
| 11            | num_total_trainings      | Total trainings attended                                                    |
| 12            | num_repeat_trainings     | Trainings attended after the first                                          |
| 13            | days_to_second_training  | Days between first and second training                                      |
| 14            | has_second_training      | Whether a second training occurred (1 = yes, 0 = no)                        |
| 15            | num_unique_trainers      | Number of distinct trainers engaged                                         |
| 16            | adopted_within_07_days  | Target: adoption within 07 days of first training (1 = yes, 0 = no)       |
| 17            | adopted_within_90_days  | Target: adoption within 90 days of first training (1 = yes, 0 = no)       |
| 18            | adopted_within_120_days  | Target: adoption within 120 days of first training (1 = yes, 0 = no)       |

## Evaluation Metric
A multi-metric evaluation:

    1. Log Loss (75%): To encourage the model to output probability estimates by penalizing confident but incorrect predictions more heavily.
    
    2. ROC-AUC (35%): To measure the model’s ability to rank adopters above non-adopters across all possible thresholds to provide a stable assessment of overall ranking since the dataset is imbalanced. 

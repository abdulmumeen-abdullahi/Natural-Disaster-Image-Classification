# Natural Disaster Damage Image Classification
## 🔹 Problem Statement
Natural disasters are events we hope to avoid, yet when they occur, rapid intervention and damage assessment become critical. Manually classifying disaster images can be tedious and time-consuming, especially with large datasets. <br/>
This project addresses that by automating the classification of natural disaster images using deep learning. Leveraging a ResNet50-based model, the system enhances situational awareness and post-disaster damage assessments by identifying disasters such as Flood, Sinkhole, Earthquake, and Forest Fire with over 98% accuracy. This contributes to faster disaster response and aligns with Sustainable Development Goals (SDGs) like: <br/>
- SDG 11: Sustainable Cities and Communities
- SDG 13: Climate Action

## 🔹 Dataset Description
- Source: [Roboflow](https://universe.roboflow.com/model-v3/natural-disaster-damage-8txjn/dataset/1)
- Total Images: 757
- Classes: 4
- Flood Damage: 193 images
- Sinkhole: 191 images
- Earthquake: 196 images
- Forest Fire: 177 images
#### Image Samples:

![download](https://github.com/user-attachments/assets/736d569f-fffd-49dd-b865-88b8285a2a31)
![download](https://github.com/user-attachments/assets/77ac406e-5cc4-4083-8010-b86fb5b4f678)
![download](https://github.com/user-attachments/assets/4bef24ba-8352-470b-afbb-c13ca181922c)
![download](https://github.com/user-attachments/assets/29696b76-1582-4fa3-977b-ae95debc944d)

## 🔹 Methodology
### 1. Data Preprocessing
- Dataset loaded using ImageFolder
- Class-wise sample display and count
- Split: 80% Training | 20% Validation
- Normalization using computed mean and standard deviation
- Data Augmentation (training only): Resize, Flip, Rotate
- Validation set: Only normalized

![Screenshot (130)](https://github.com/user-attachments/assets/7bfd5fd1-e831-4342-8f0b-177281229ae1)

### 2. Model Training & Evaluation
- Model: ResNet-50 (pretrained)
- Modified Head: Linear(2048 → 256) → ReLU → Dropout → Linear(256 → 4)
- Training Details: <br/>
      - Epochs: 50 (Early stopped at 38) <br/>
      - Framework: PyTorch <br/>
      - Cross-validation: 5-fold <br/>

## 🔹 Performance Metrics
- Accuracy: 99.74%
- Precision: 99.74%
- Recall: 99.72%
- F1 Score: 99.73%
- #### Aggregate Accuracy Score for the model was calculated
- #### Precision, Recall, and F1 Score for each of the classes was calculated

![Screenshot (131)](https://github.com/user-attachments/assets/963cea12-7739-4a48-a5a7-8df5c59a5734)

- #### The confusion matrix of the model was calculated and visualized, revealing high True Positives across all classes and very few misclassifications, indicating strong model performance with low False Positives and False Negatives


![download](https://github.com/user-attachments/assets/0ba1d98e-a551-4d21-9175-1175d91dbccc)

## 🔹 Model Summary
| Metric               | Value      |
|:---------------------|:----------:|
| Total Parameters     | 24,033,604 |
| Input Size           | 19.27 MB   |
| Parameters Size      | 96.13 MB   |
| Estimated Model Size | 5805.83 MB |

## 🔹 Real-World Applications
- Post-Disaster Damage Assessment
- Disaster Type Mapping for Rescue Planning
- Satellite Image Processing in Emergency Response
- Support for Government/NGO Relief Resource Allocation

## 🔹 Environmental Impact
Helps minimize human risk during disaster response by enabling safer, AI-assisted remote assessments. Contributes to more efficient climate resilience strategies.

================================================= <br/>
Abdullahi Olalekan Abdulmumeen <br/>
Data Scientist | Computer Vision Engineer <br/>
olalekanabdulmumeen3@gmail.com <br/>
+2347053053024

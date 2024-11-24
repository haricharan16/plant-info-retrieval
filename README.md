# Plant Classifier and Information Retrieval

This project aims to classify plant species and retrieve detailed information about them using a combination of deep learning and information retrieval techniques. It is implemented in three major steps: **Data Collection and Preparation**, **Plant Detection**, and **Information Retrieval**.

---

## Table of Contents
1. [Data Collection and Preparation](#data-collection-and-preparation)
2. [Plant Detection](#plant-detection)
3. [Information Retrieval](#information-retrieval)
4. [Results](#results)
5. [Requirements](#requirements)
6. [Usage](#usage)

---

## Data Collection and Preparation

### Description
The first step involves collecting a diverse dataset of plant species. Our custom dataset includes **19 types of plants**, each represented by multiple images. To ensure robustness and improve model performance, the dataset was augmented using various techniques such as:
- Rotation
- Scaling
- Flipping
- Color adjustment

### Key Steps:
1. **Data Collection**: Dataset is collected from the institute herbal garden from 19 plants.
2. **Data Augmentation**: Applied augmentation techniques to expand the dataset and introduce variations for better generalization.
3. **Dataset Organization**: The dataset was structured into training and testing sets.

---

## Plant Detection

### Description
The second step focuses on detecting and classifying plants using a **ResNet50** model. The model was trained on the prepared dataset to identify the 19 plant types.

### Key Metrics:
- **Training Accuracy**: The model achieved a **95.95% train accuracy**.



### Additional Feature:
During testing, the model computes a **similarity score** for a given plant leaf against every plant in the dataset. Based on this score, the **top 5 most similar plants** are identified for further processing.

---

## Information Retrieval

### Description
To extract detailed information about the top 5 similar plants, a **Dense Passage Retrieval (DPR)** model was used. The DPR model retrieves relevant information by:
1. **Fine-tuning**: The pretrained DPR model was fine-tuned on a custom dataset curated specifically for this project to improve performance on plant-related queries.
2. **Querying**: Information about the top 5 similar plants was retrieved using their latent vector representations.

This step ensures accurate and contextually relevant details about the identified plants are available for further analysis.

---

## Results

- **Plant Classification Test Accuracy**: 94.49%

- **Information Retrieval**: Successfully retrieved detailed information for the top 5 similar plants for any given input leaf.

---

## Requirements

- Python 3.8+
- PyTorch
- Transformers library (for DPR)
- Pandas, NumPy, Matplotlib


## Contributors

- **B HariCharan Goud**  
  *IIT Bhilai, Data Science and Artificial Intelligence*
- **Kemasaram Nithin**
   *IIt Bhilai, Data Science and Artificial Intelligence*
- **Ganta Srujan**
    *IIT Bhiali, data Science and Artificial Intelligence*


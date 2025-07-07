# CNN-Comparison-Project
This project compares three Convolutional Neural Networks (CNNs) designed for binary classification of HER2 status in IHC-stained breast cancer biopsy images. <br>
### Dataset
The dataset was obtained from the Breast Cancer Immunohistochemistry (BCI) project, and contains IHC-stained histopathology images labeled for HER2 expression: https://bupt-ai-cz.github.io/BCI/<br>
### Methods
* Implemented and trained three CNN architectures using PyTorch
* Utilized the Adam optimizer with varying learning rates depending on the model
* Employed BCEWithLogitsLoss with a positive class weighting (pos_weight) to address class imbalance
* Trained models using GPU accelearation via CUDA when available
* Evaluated model performance on both training and validation sets using:
    - Accuracy
    - Precision
    - Recall
    - ROC-AUC
* Tracked training loss across epochs and visualized with Matplotlib
### Results
* #### CNN #1 (LeNet-Based)
  Training Set:
  * Accuracy: 83.1%
  * Precision: 94.6%
  * Recall: 80.9%
  * ROC AUC: 0.940 

  Validation Set:
  * Accuracy: 70.6% 
  * Precision: 83.8%
  * Recall: 72.3%
  * ROC AUC: 0.778

* #### CNN #2 (AlexNet-Based)
  Training Set: 
  * Accuracy: 71.2%
  * Precision: 78.7%
  * Recall: 81.9%
  * ROC AUC: 0.769

  Validation Set:
  * Accuracy: 71.0%
  * Precision: 78.1%
  * Recall: 81.8%
  * ROC AUC: 0.776

* #### CNN #3 (HAHNet-Based with Inception Block Architecture)
  Training Set:
  * Accuracy: 71.9%
  * Precision: 71.9%
  * Recall: 99.2%
  * ROC AUC: 0.808

  Validation Set:
  * Accuracy: 72.4%
  * Precision: 72.7%
  * Recall: 98.9%
  * ROC AUC: 0.819

### Notes
This project demonstrates the trade-offs between precision and recall in medical image classification tasks.

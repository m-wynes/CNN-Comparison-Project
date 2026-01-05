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

| Model | Dataset | Accuracy | Precision | Recall | ROC-AUC |
| --- | --- | --- | --- |--- |--- |
| LeNet-Based | Training | 83.1% | 94.6% | 80.9% | 0.940 |
| | Validation | 70.6% | 83.8% | 72.3% | 0.778 |
| AlexNet-Based | Training | 71.2% | 78.7% | 81.9% | 0.769 |
| | Validation | 71.0% | 78.1% | 81.8% | 0.776 |
| HAHNet-Based with Inception Block Architecture | Training | 71.9% | 71.9% | 99.2% | 0.808 |
| | Validation | 72.4% | 72.7% | 98.9% | 0.819 |

### Conclusion
The purpose of this project was to evaluate three different CNN architectures created to classify HER2 status in breast cancer histopathology images. Between the models, the HAHNet-Based with Inception Block Architecture architecture proved to have the best ability to generalize unseen images and maintain a high perceptiveness for the HER2 positive samples. This is critical for clinical diagnostic settings, as false negatives could be devastating to a patient’s treatment plan and their disease outcome. Despite this success, the model can still be improved upon. One of the current limitations is the precision score, which indicates there is a need to minimize the number of false positive predictions. Future versions of this model may increase the precision score by adjusting the weight formula or augmenting the dataset, both of which would offset the class imbalance. 

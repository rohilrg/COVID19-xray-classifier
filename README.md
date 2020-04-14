# COVID19-xray-classifier
A classifier that takes X-RAY or CT-SCAN to classify positive or negative COVID19 with 99% accuracy, 97% recall (macro avg) and 91% precision (macro avg).

## Data Preparation
The data for training the model was gathered from two sources:
1. COVID19 X-RAY images repository: https://github.com/ieee8023/covid-chestxray-dataset
2. Chest X-Ray Images (Pneumonia) on Kaggle: https://www.kaggle.com/paultimothymooney/chest-xray-pneumonia

The preprocessing and cleaning of images/labels was done to ensure data in correct form. For further reference of the process please check this notebook https://www.kaggle.com/rgaltro/covid19-data-preprocessing.

## Training of model
Different models were trained like VGG16, Autoencoder classifier and InceptionV3. In the end InceptionV3 produced the best results.
### Note:
To tackle the high imblance of data, different class weights were used.

## Evalutation and results

The dataset was divided into train, validation and test set beforhand to ensure the sanity of further process. 

The model was selected while training which had the highest val_accuracy.

### Sample output of the test-set images:

![COVID-19 Positive patient](https://github.com/rohilrg/COVID19-xray-classifier/blob/master/helper_images/sample_output.png)
![COVID-19 Negative patient](https://github.com/rohilrg/COVID19-xray-classifier/blob/master/helper_images/sample_output2.png)
![COVID-19 Positive patient](https://github.com/rohilrg/COVID19-xray-classifier/blob/master/helper_images/sample_output_3.png)

### Confusion matrix for test-set images

![Confusion Matrix non-norm](https://github.com/rohilrg/COVID19-xray-classifier/blob/master/helper_images/Confusion_matrix_nonnor.png)
![Confusion Matrix norm](https://github.com/rohilrg/COVID19-xray-classifier/blob/master/helper_images/Confusion_matrix_nor.png.png)

### Classification report of the trained model on test-set images

![Classification Report](https://github.com/rohilrg/COVID19-xray-classifier/blob/master/helper_images/classification_report.png)

### ROC curve 

![ROC curve](https://github.com/rohilrg/COVID19-xray-classifier/blob/master/helper_images/roc_curve.png)

# Conclusion

The InceptionV3 model with modified head converged to classifiy the prositive and the negative cases of COVID19 with 99% accuracy, 97% recall (macro avg) and 91% precision (macro avg).

# Further work

The model can be further improved with more COVID19 positive cases for training.

# Note:
This work was inspired from the work of Hanan Gani work at: https://github.com/hananshafi/covid19-detection

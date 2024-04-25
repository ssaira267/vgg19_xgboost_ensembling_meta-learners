# **Ensembling XGBoost models with Logistic Regression as Meta-Learner**
### This repository contributes to Chapter 6 of Saira Baharuddin's PhD thesis, entitled "Multimodal Learning for Carbonate Rock Classification Using Microresistivity Images and Wireline Logs".

## Abstract
The XGBoost model trained using the standard wireline log achieved high accuracy (91%), whereas the models trained with VGG19 CNN feature extraction showed lower accuracy due to overfitting. In this chapter/study, I explore the use of multimodal learning by combining FMS images and wireline log data to attempt to improve the models’ predictive performance. Here, I ensemble the XGBoost models trained on tabular and image data with a final logistic regression and compare the performance to the single-modal learning. 

<p align="center">
    <img width="300"  alt="ensemble" src="https://github.com/ssaira267/vgg19_xgboost_ensembling_meta-learners/assets/57672761/de8c753f-64dc-43f8-88ad-e42365d72861">
</p>
<p align="center">
Ensembling, or stacking classifier proposed as part of multi-modal learning.
</p>

The model achieved an overall accuracy of 87% and 83% depending on the datasets used. The ensemble models do not perform better when compared to the XGBoost model trained only on tabular wireline log data. This is likely due to the poor performance of the XGBoost image models trained during single modal learning, which presented challenges in integrating multimodal data when one model is considerably weaker. 

## Repository Contents
1. Data: Sample datasets used for training and testing the models are publicly available on the following website: https://mlp.ldeo.columbia.edu/logdb/scientific_ocean_drilling. The dataset used are from Leg 194, holes 1194B, 1196A and 1199A. The .csv files inside the data directory serve as examples demonstrating how the data is arranged and used for this study. These files contain structured data in tabular format, where each row represents a sample or observation based on depth, and each column represents a feature or attribute of that sample. Due to the large file size of the FMS images, I am unable to upload the FMS images folder. However, the images are available on the website mentioned earlier. It's important to note that the FMS images have been cropped based on the depth intervals specified for the study.
2. Notebooks: Python codes developed include data preprocessing, model training, model evaluation, and visualization of the results.
3. Documentation: Additional resources and documentation that outline the methods used in this study.

## How to Use
To run the scripts in this repository:
1. Ensure that Python 3.8 (and above) and the necessary libraries (listed in requirements.txt) are installed.
2. Clone the repository to your local machine.
3. Navigate to the notebooks directory and run the desired notebook as follows:
  
  ```bash
  python notebook_name.py
  ```

## Dependencies 
- Dlisio
- Imbalanced-learn
- Livelossplot
- Matplotlib
- NumPy
- OpenCV-python
- pandas
- Scikit-learn
- Seaborn
- Tensorflow
- Tensorflow-Keras
- XGBoost

Please refer to 'requirements.txt' for a complete list of dependencies.

## Contact
For any queries related to this repository or the research, please contact:
- Saira Baharuddin                  - Email: s.baharuddin19@imperial.ac.uk
- Prof Cédric John (PhD Supervisor) - Email: cedric.john@qmul.ac.uk

# Imbalanced_Data
A notebook whose focus is to prepare imbalanced data in order to be able to detect the minority class.

**DATA**
Extracted from the opnml website and can be downloaded at https://www.openml.org/d/1461. While in the notebook I use the _fetch_openml()_ function, I provide a csv as well in the _Data_ folder.

The Data consists of 17 columns and 45211 entries. Of those 17 columns, the target is the attribute **class** which tells if the client has subscribed for a long term deposit or not.

**OBJECTIVE**
The focus while working on this notebook is to prepare the data in the best way possible to feed it into a classification algorithm that will predict whether the client will subscribe to a long term deposit or not. In order to do so, the imbalance in the data will have to be addressed. 

Out of the 45211 instances:
- 39922 belong to _class_1_ 
- 5289 belong to _class_2_. 

This will, inevitably, cause a bias in the algorithms that train with this data, being really eager to classify each new instance as _class_1_.

**How will this by fixed?**
Three approaches will be used in this notebook:

1. Downsampling the majority class.
2. Upsampling the minority class.
3. Generating synthetic samples (SMOTE)


There will only be one algorithm implemented, a Random Forest, since the focus of this notebook is just to address the imbalanced data.

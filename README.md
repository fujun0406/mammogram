# Project - Mammogram mass

## Contents
* [Background](#background)
* [Dataset](#dataset)
* [Results](#results)

## Background
Mammography is an effective way of using low-energy X-rays to examine human breast and diagnose breast cancer. However, the low positive predictive value of breast biopsy causing by mammography which lead to approximately 70% biopsy with benign mass. In order to reduce the high number of unnecessary biopsy, we want to build a model which can classify severity of mass based on some features.

## Dataset
Thes data come from a paper published by Elter, et al (source: http://archive.ics.uci.edu/ml/datasets/mammographic+mass). 

This dataset contain 961 instances of masses detected in mammograms and 6 attributes as following:

* `BI-RADS` - 1 to 5 (ordinal)  
* `age` - patient's age in years (integer)
* `shape` - mass shape: round=1 oval=2 lobular=3 irregular=4 (nominal)
* `margin` - mass margin: circumscribed=1 microlobulated=2 obscured=3 ill-defined=4 spiculated=5 (nominal)
* `density` - mass density high=1 iso=2 low=3 fat-containing=4 (ordinal)
* `severity` - benign=0 or malignant=1 (binominal)
 
The feature of `BI-RADS` is an assessment of how confident the severity classification is. 

For this project, we are tasked with developing a classification model for assessed the severity of mammogram mass. Since the feature of `BI-RADS` is relative with severity, we will consider to use `age`, `shape`, `margin` and `density` to build model. We will try some models as following,

## Results
We build some model toward this data set and the result shows as following.

| Model                  | Accuracy   | 
|:----------------------:|:----------:|
| Decision Tree          | 74.1%      |
| SVM with linear kernel | 79.7%      |
| SVM with rbf kernel    | 77.4%      |
| KNN                    | 78.0%      |
| Logistic Regression    | 80.7%      |
| Keras in scikit-learn  | 79.7%      |

We can see that the accuracy of most algorithm is 77-81% but deciosn tree is the less one with 74.1%. If we consider hyperparameter or different topologies, the result may be different.

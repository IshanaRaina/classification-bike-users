## Customer Segmentation using Classification :family:

In order to increase adoption for this system the number of subscribers need to be increased, that is, people who purchase Bay Area Bike Share's service for a given period of time. The first step towards this :dart: is to understand what features constitute a subscriber. And what better way to deduce the differences between a **Customer** and **Subscriber** than classification! 

Different techniques are used to classify _Subscriber Type_ and then evaluated on performance. Here's a quick overview:

Algorithm | Accuracy
--- | ---
Naive Bayes Classifier | 74.52%
AdaBoost | 82.32
Bagging | 82.87%
Decision Tree Classifier | 90.95%

### Naive Bayes Classification

**Precision - 76.9%**
**Recall - 70.1%**
**Correctly Classified Instances - 74.52%**

Reason for low accuracy:
- Attributes are treated as though they are completely independent of one another.
- Each attribute contributes to the model equally. 

### AdaBoost

**Correctly Classified Instances - 82.32%**

Reason for low accuracy:
- Can be sensitive to noisy data and outliers. 

### Bagging

**Correctly Classified Instances - 82.87%**

Reason for low accuracy:
- Bagging bad classifiers can degrade their performance even further. 

### Decision Tree Classification

Performs the best of them all :tada:

![](https://i.imgur.com/uDtz1CW.png)

The instances have been classified into class label **Customer** or **Subscriber** based on _Duration_ and _Day_ attributes. Here _Duration_ is a continuous variable (represented in minutes) and is split according to the best cut. On the other hand, _Day_ is a categorical variable taking on 2 values - `Weekday` or `Weekend`.

![](https://i.imgur.com/cf0Hwep.png)

# Hello World of Machine Learning : MNIST Dataset
In this project MNIST dataset is used  which is a set of 70,000 small images of digits handwritten by Highschool students and employees of the US census Bureau.  
Each image is labeled with the digit it represents .  
Thes set has been studied so much that it is often called the "hello world" of Machine Learning .  
Whenever people come up with new classification algorithm they are curious to see how it will perform on MNIST,and anyone who learns ML tackles this dataset sooner or later.
## Let's see some of the images :
![more digits](https://github.com/Zahid8889/CLassification-MNIST-Hello-world-of-ML/assets/102400053/89e8bce2-ef71-4f0d-87a1-25ee68d3ea6a)
## Binary Classifier
### First we have trained a binary classifier to classify the 5's or the 5-detector.
We have starded with Stochastic Gradient Descent of scikit learn.
This Classifier has the advantage of handling very large dataset efficiently,partly because it deals with training instanced independently.
### Then we have used various performance measures to check which is a good performance measure
#### Accuracy
- We observed that simply accuracy can not be used for the performance measure because in case of skewed datasets we can get a false idea of a good performing model.
#### Confusion MAtrix
- A much better way to evaluate the performance of a classifier is to look at the confusion matrix.
- Each row in a Confusion Matrix represent an actual class , while each column represent a predicted class.
#### Precision
- The confusion metrix gives us a lot of information but sometime we prefer a more consise metric.
- An interesting way to look at is<b> the accuracy of the positive predictions.</b> this is called precision of classifier.
#### Recall
- Precision typically used along with another metric named Recall, also called <i>sensitivity</i> or the <i> true positive rate</i>.
- This is the ratio of positive instances that are correctly detected by the classifier
### Precision and Recall Tradeoff
- Unfortunately we can't increase both precision and recall , incresing precision reduces recall and vice versa.
- This is called precision recall tradeoff.
- Let us see the precision recall vs the threshold of the Stochastic Gradient Descent Classifier Decision function.
 ![precision_recall_vs_threshold_plot](https://github.com/Zahid8889/CLassification-MNIST-Hello-world-of-ML/assets/102400053/73023b27-000f-412d-ace3-4857b37cfd0b)
- We should also see the Precision vs Recall Graph.
![precision_vs_recall_plot](https://github.com/Zahid8889/CLassification-MNIST-Hello-world-of-ML/assets/102400053/0779cea2-2159-4a00-81a3-2796d57fb647)
- The Red mark is at the 90% precsion .
### ROC Curve
- The Reciever Operating Characteristic (ROC) Curve is another common tool used with Binary Classifier.
- It is very similer to the precision / recall curve, but
- instead of plotting precision vs recall, The ROC curve plots the  <i><b>true positive rate</b></i> (another name for recall) against the <i><b> false positive rate</i></b>.
- let us see the ROC curve for our SGD classifier.
![roc_curve_plot](https://github.com/Zahid8889/CLassification-MNIST-Hello-world-of-ML/assets/102400053/a7dbddb2-c6ec-470b-bd12-60c11465e9f9)
- The dotted line represents the ROC curve of a purely random classifier, a good classifier stays far away from that line as possible toward top-left corner.
#### Comparing ROC curve SGD vs RANDOM FOREST
![ROC_CURVE_COMPARISON](https://github.com/Zahid8889/CLassification-MNIST-Hello-world-of-ML/assets/102400053/2cb1a200-7b8c-4cff-9970-6301d611f13a)
- The Random Forest Classifier is siperior to the sgd classifier because its ROC curve is much closer to the ltop left corner and it has greater Area Under Curve.
- 

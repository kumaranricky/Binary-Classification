### EX NO: 02

### DATE: 


# <p align = "center"> BINARY CLASSIFICATION </p>
## <br>Aim:
To write a python program to perform binary classification.

## <br> Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner /Google Colab

## <br> Related theoritical concepts
 
Binary classification is a form of classification — the process of predicting categorical variables — where the output is restricted to two classes. It is used in many different data science applications, such as Medical Diagnosis, Email analysis, Marketing, etc. For example, in medical diagnosis, a binary classifier for a specific disease could take in symptoms of a patient and predict whether the patient is healthy or has a disease. The possible outcomes of the diagnosis are positive and negative.

## <br> Algorithm
1.define dataset.\
2.summarize dataset shape.\
3.summarize observations by class label.\
4.summarize first few examples.\
5.plot the dataset and color the by class label


## <br><br><br><br><br>Program:
```
/*
Program to implement binary classification.
Developed by:KUMARAN B
RegisterNumber: 212220230026
*/
```
```python
from numpy import where
from collections import Counter
from sklearn.datasets import make_blobs
from matplotlib import pyplot

X,y = make_blobs(n_samples=10,centers=2,random_state=1)
print(X.shape,y.shape)
counter=Counter(y)
print(counter)

for i in range(5):
    print(X[i],y[i])
    
for label, _ in counter.items():
    row_ix=where(y==label)[0]
    pyplot.scatter(X[row_ix,0], X[row_ix,1], label=str(label))
pyplot.legend()
pyplot.show()
```

## <br><br><br><br><br><br><br><br><br><br><br><br>Output:

![Screenshot (1)](https://user-images.githubusercontent.com/75235334/163752778-9729c706-24d7-4db6-9f7d-91f381151104.png)



## <br><br><br><br> <br><br><br><br><br><br>Result:
Thus the python program performed binary classification successfully.

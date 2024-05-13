# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. 
2. 
3. 
4. 

## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: PADMASHREEE R
RegisterNumber:  212222040110
*/

import pandas as pd
data=pd.read_csv("/content/spam.csv",encoding='Windows-1252')
from sklearn.model_selection import train_test_split
data
data.shape
x=data['v2'].values
y=data['v1'].values
x.shape
y.shape
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.35,random_state=0)
x_train
x_train.shape
from sklearn.feature_extraction.text import CountVectorizer
cv=CountVectorizer()
x_train=cv.fit_transform(x_train)
x_test=cv.transform(x_test)
from sklearn.svm import SVC
svc=SVC()
svc.fit(x_train,y_train)
y_pred=svc.predict(x_test)
y_pred
from sklearn.metrics import accuracy_score,confusion_matrix,classification_report
acc=accuracy_score(y_test,y_pred)
acc
con=confusion_matrix(y_test,y_pred)
print(con)
cl=classification_report(y_test,y_pred)
print(cl)
```

## Output:
![image](https://github.com/PadmashreeRajesh/Implementation-of-SVM-For-Spam-Mail-Detection/assets/119393915/3a4807c1-d7f1-47f3-bc70-2e97426b14ac)

![image](https://github.com/PadmashreeRajesh/Implementation-of-SVM-For-Spam-Mail-Detection/assets/119393915/a8b446f4-fad3-4a96-a441-b3132e3bc8cd)

![image](https://github.com/PadmashreeRajesh/Implementation-of-SVM-For-Spam-Mail-Detection/assets/119393915/a794a596-955e-44b1-9524-fc80da39ac68)

![image](https://github.com/PadmashreeRajesh/Implementation-of-SVM-For-Spam-Mail-Detection/assets/119393915/a91fbb7d-f43c-474b-8d2d-41e5c5984ac0)

![image](https://github.com/PadmashreeRajesh/Implementation-of-SVM-For-Spam-Mail-Detection/assets/119393915/ce71a869-5486-4c48-b7c4-ae4fffa60290)

![image](https://github.com/PadmashreeRajesh/Implementation-of-SVM-For-Spam-Mail-Detection/assets/119393915/99fdf39f-5be7-49e3-b066-c82015939648)

![image](https://github.com/PadmashreeRajesh/Implementation-of-SVM-For-Spam-Mail-Detection/assets/119393915/c622d80c-113d-4734-b8b4-c1bfb7bd6077)

![image](https://github.com/PadmashreeRajesh/Implementation-of-SVM-For-Spam-Mail-Detection/assets/119393915/ffb57456-7d48-4319-9dec-526e8a2e7f9d)

![image](https://github.com/PadmashreeRajesh/Implementation-of-SVM-For-Spam-Mail-Detection/assets/119393915/5c9b0034-7fa1-41e9-83a7-95fd5af764af)

## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.

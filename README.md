Developed by: JAYANI N

RegisterNumber:  212224100025


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
*/
```
        import pandas as pd
        data=pd.read_csv("/content/spam.csv",encoding="Windows-1252")
        data.info()
        
        x=data['v2'].values
        y=data['v1'].values
        x.shape
        y.shape
        
        from sklearn.model_selection import train_test_split
        x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=2)
        
        from sklearn.feature_extraction.text import CountVectorizer
        cv=CountVectorizer()
        x_train=cv.fit_transform(x_train)
        x_test=cv.transform(x_test)
        x_train
        
        from sklearn.svm import SVC
        svc=SVC()
        svc.fit(x_train,y_train)
        y_pred=svc.predict(x_test)
        y_pred
        
        from sklearn.metrics import accuracy_score
        acc=accuracy_score(y_test,y_pred)
        acc


## Output:




## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.

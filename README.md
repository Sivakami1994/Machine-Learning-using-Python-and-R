# Machine-Learning-using-Python-and-R
Machine Learning code 
# Importing the libraries
import numpy as np
import matplotlib.pyplot as plt
import pandas as pd

# Importing the dataset
dataset = pd.read_csv('Data.csv')
X=dataset.iloc[:,:-1].values
Y=dataset.iloc[:,3].values

#taking care of missing data

from sklearn.preprocessing import Imputer
imputer=Imputer(missing_values='NaN',strategy='mean', axis=0)
imputer=imputer.fit(X[:,1:3])
X[:,1:3]=imputer.transform(X[:,1:3])

#importing the dataset
dataset=read.csv('Data.csv')

#handling the missing data
dataset$Age = ifelse(is.na(dataset$Age),
                     ave(dataset$Age,FUN=function(X)mean(X, na.rm=TRUE)),
                     dataset$Age)
dataset$Salary = ifelse(is.na(dataset$Salary),
                     ave(dataset$Salary,FUN=function(X)mean(X, na.rm=TRUE)),
                     dataset$Salary)

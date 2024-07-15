# DIABETES_ANALYSIS
# importing libararies
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

data = pd.read_csv("diabetes2.csv")
data['sum'] = data.sum(axis=1)
data.head(15)
x = data["Glucose"]
y = data["Outcome"]
plt.scatter(x, y)
plt.show()
# if i want to check that values are null or not
data.isnull().sum()
# data summary
data.count()
# coloumns and rows
data.shape
# statistical measures
data.describe()
# how many are diabetic or non diabetic
data['Outcome'].value_counts()
# visualizing outcomes wrt age
import seaborn as sns
sns.countplot(x=data['Age'], hue=data['Outcome'])
# visualizing outcomes wrt pregnancies
import seaborn as sns
sns.countplot(x=data['Pregnancies'], hue=data['Outcome'])
# conclusion
there are more non diabetic persons then diabetic


# Python_Time_Series

# Titanic - Machine Learning from Disaster

## Content of the project
This project (still a WIP!) uses machine learning to create a model that predicts which passengers survived the Titanic shipwreck. More details can be found in Kaggle's website: https://www.kaggle.com/competitions/titanic 


## Instructions
Three files are provided by Kaggle:
- `train.csv`: this is the training file. It contains all of the variables needed for the analysis (see below). The PassengerId included go from 1 to 891.
- `test.csv`: this is the testing file. It contains the same variables as the train.csv file, except for the one we are trying to predict (Survival). The PassengerId included go from 892 to 1309.
- `gender_submission.csv`: it contains the survival information of the passangers that are included in the test.csv file

The variables containes in the datasets are:
- `survival`: 0 = No, 1 = Yes
- `pclass`: 1 = 1st, 2 = 2nd, 3 = 3rd
- `sex`:	Sex
- `Age`:	Age in years	
- `sibsp`:	# of siblings / spouses aboard the Titanic
- `parch`:	# of parents / children aboard the Titanic
- `ticket`:	Ticket number
- `fare`:	Passenger fare
- `cabin`:	Cabin number
- `embarked`:	Port of Embarkation	(C = Cherbourg, Q = Queenstown, S = Southampton)

When running the code, make sure that the filepath for the several read_excel and read_csv Panda functions have been updated correctly.


## Rationale and Methodology

### Data Exploration


### Feature Engineering
The following are the main transformations performed in the dataset:
- Delete the Fare column. The reason is that it is very correlated with the Class column
- Delete the Ticket column, given that it was difficult to extract any information from it
- Delete the Cabin column, given that more than 50% of it is NA
- Fill out the NAs of the Age column with
    those who have “Master” in the Name column have taken the average of “Master”
    the same applies for the “Miss”
    the rest have taken the average of the remaining values
- The Alone column is 1 if both SibSp and Parch are 1, 0 otherwise
- The Age_Children (omitted) encompasses people who are below 16 years old, Age_Adult from 16 to 50, and Age_Elderly those who are older
- Delete the Name column and the Age column


### Machine Learning Methodology


### Results and Discussion



## Usage

To run the analysis, open the `titanic_julian_enciso.ipynb` notebook and execute each cell sequentially. Ensure that the required datasets are in the correct file paths.


## Dependencies

The following libraries are used in different parts of the project:
- Pandas
- Numpy
- Matplotlib.pyplot
- Seaborn
- Os
- Xgboost
- Lightgbm
- Sklearn.ensemble
- Sklearn.linear_model
- Sklearn.svc
- Sklearn.neighbors
- Sklearn.naive_bayes
- Sklearn.tree
- Sklearn.model_selection
- Sklearn.preprocessing
- Sklearn.metrics


Proceed to their installation with the following code:

```
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
import os
import xgboost as xgb
import lightgbm as lgb
from sklearn.ensemble import RandomForestClassifier
from sklearn.linear_model import LogisticRegression
from sklearn.svm import SVC
from sklearn.neighbors import KNeighborsClassifier
from sklearn.naive_bayes import GaussianNB
from sklearn.tree import DecisionTreeClassifier
from sklearn.model_selection import train_test_split, cross_val_score
from sklearn.preprocessing import StandardScaler
from sklearn.metrics import accuracy_score, classification_report, confusion_matrix
```

## Installation
Ensure that you have Python installed on your system. If not, you can download it from [python.org](https://www.python.org/downloads/).


## Usage
You are allowed to view and fork the repository for personal use. If you have any questions or would like to discuss potential collaborations, feel free to reach out.


## Contributing
Although this project is not open-source, I welcome feedback, bug reports, and suggestions. If you encounter any issues or have ideas for improvements, feel free to send me an email to julian.enciso.izquierdo@gmail.com.


## License
This project is not open-source, and it does not come with a specific open-source license. All rights are reserved, and usage, modification, or distribution of the code is not permitted without explicit permission.

If you are interested in using or collaborating on this project, please send me an email to julian.enciso.izquierdo@gmail.com.


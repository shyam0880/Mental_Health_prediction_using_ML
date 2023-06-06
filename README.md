# Mental_Health_prediction_using_ML
The project develops a ML solution by implementing multiple algorithms to solve a specific problem. Through rigorous evaluation, the project assesses algorithm performance considering accuracy, speed, and resource requirements. The best algorithm is selected based on optimal results, balancing efficiency and effectiveness.

Data= GitHub\Mental_Health_prediction_using_ML\survey.csv

###df.shape
The dataset contains 1259 rows and 27 columns.

#name of the column
df.columns

Index(['Timestamp', 'Age', 'Gender', 'Country', 'state', 'self_employed',
       'family_history', 'treatment', 'work_interfere', 'no_employees',
       'remote_work', 'tech_company', 'benefits', 'care_options',
       'wellness_program', 'seek_help', 'anonymity', 'leave',
       'mental_health_consequence', 'phys_health_consequence', 'coworkers',
       'supervisor', 'mental_health_interview', 'phys_health_interview',
       'mental_vs_physical', 'obs_consequence', 'comments'],
      dtype='object')

# prints information about the DataFrame
df.info()

Data columns (total 27 columns):
 #   Column                     Non-Null Count  Dtype 
---  ------                     --------------  ----- 
 0   Timestamp                  1259 non-null   object
 1   Age                        1259 non-null   int64 
 2   Gender                     1259 non-null   object
 3   Country                    1259 non-null   object
 4   state                      744 non-null    object
 5   self_employed              1241 non-null   object
 6   family_history             1259 non-null   object
 7   treatment                  1259 non-null   object
 8   work_interfere             995 non-null    object
 9   no_employees               1259 non-null   object
 10  remote_work                1259 non-null   object
 11  tech_company               1259 non-null   object
 12  benefits                   1259 non-null   object
 13  care_options               1259 non-null   object
 14  wellness_program           1259 non-null   object
 15  seek_help                  1259 non-null   object
 16  anonymity                  1259 non-null   object
 17  leave                      1259 non-null   object
 18  mental_health_consequence  1259 non-null   object
 19  phys_health_consequence    1259 non-null   object
...
 25  obs_consequence            1259 non-null   object
 26  comments                   164 non-null    object
dtypes: int64(1), object(26)
memory usage: 265.7+ KB

# returns the number of unique values for each column
df.nunique()

Timestamp                    1246
Age                            53
Gender                         49
Country                        48
state                          45
self_employed                   2
family_history                  2
treatment                       2
work_interfere                  4
no_employees                    6
remote_work                     2
tech_company                    2
benefits                        3
care_options                    3
wellness_program                3
seek_help                       3
anonymity                       3
leave                           5
mental_health_consequence       3
phys_health_consequence         3
coworkers                       3
supervisor                      3
mental_health_interview         3
phys_health_interview           3
mental_vs_physical              3
obs_consequence                 2
comments                      160
dtype: int64

#printing the options of attributes(column 1: yes, no, nan)
for i in df_cat.columns:
  print(df_cat[i].unique())

[nan 'Yes' 'No']
['No' 'Yes']
['Yes' 'No']
['Often' 'Rarely' 'Never' 'Sometimes' nan]
['6-25' 'More than 1000' '26-100' '100-500' '1-5' '500-1000']
['No' 'Yes']
['Yes' 'No']
['Yes' "Don't know" 'No']
['Not sure' 'No' 'Yes']
['No' "Don't know" 'Yes']
['Yes' "Don't know" 'No']
['Yes' "Don't know" 'No']
['Somewhat easy' "Don't know" 'Somewhat difficult' 'Very difficult'
 'Very easy']
['No' 'Maybe' 'Yes']
['No' 'Yes' 'Maybe']
['Some of them' 'No' 'Yes']
['Yes' 'No' 'Some of them']
['No' 'Yes' 'Maybe']
['Maybe' 'No' 'Yes']
['Yes' "Don't know" 'No']
['No' 'Yes']


#Ploting image of attribute with it's data
image.png
.......


#boxplot of age attribute
image.png

#filtering the age
df.drop(df[df['Age'] < 0].index, inplace = True)
df.drop(df[df['Age'] > 100].index, inplace = True)

#print unique number
df['Age'].unique()

array([37, 44, 32, 31, 33, 35, 39, 42, 23, 29, 36, 27, 46, 41, 34, 30, 40,
       38, 50, 24, 18, 28, 26, 22, 19, 25, 45, 21, 43, 56, 60, 54, 55, 48,
       20, 57, 58, 47, 62, 51, 65, 49,  5, 53, 61,  8, 11, 72])

#hisplot figure
image.png

#unique data
df['Gender'].unique()

array(['Female', 'Male', 'Other'], dtype=object)


#atrribute option count
df['Gender'].value_counts()

Male      988
Female    247
Other      19
Name: Gender, dtype: int64

#figure
image

pie

#figure of attribute like (self employed) with treatement
image

#heat map
image

#accuracy of all ML algorithm
LogisticRegression 0.7898089171974523
KNeighborsClassifier 0.697452229299363
DecisionTreeClassifier 0.7484076433121019
RandomForestClassifier 0.802547770700637
GradientBoostingClassifier 0.8057324840764332
AdaBoostClassifier 0.7866242038216561
XGBClassifier 0.7961783439490446

#in figure
image

#selecting ML having high accuracy

The Algorithm which gives maximum accuracy...
GradientBoostingClassifier : 0.8057324840764332

#confusion matrix of Gradient booster
image

#ROC curve

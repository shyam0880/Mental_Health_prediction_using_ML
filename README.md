# Mental_Health_prediction_using_ML
The project develops a ML solution by implementing multiple algorithms to solve a specific problem. Through rigorous evaluation, the project assesses algorithm performance considering accuracy, speed, and resource requirements. The best algorithm is selected based on optimal results, balancing efficiency and effectiveness.
---
<U><h3 align="center" >***If you are using GitHub in  a dark mood please make it light mood, else you can't able to see the image data***</h3></U>
<br>

```bash
  Data= survey.csv
```

<p>->The dataset contains 1259 rows and 27 columns.</p>

### `Dataset column`

<p>'Timestamp', 'Age', 'Gender', 'Country', 'state', 'self_employed','family_history', 'treatment', 'work_interfere', 'no_employees','remote_work', 'tech_company', 'benefits', 'care_options','wellness_program', 'seek_help', 'anonymity', 'leave','mental_health_consequence', 'phys_health_consequence', 'coworkers',
 'supervisor', 'mental_health_interview', 'phys_health_interview','mental_vs_physical', 'obs_consequence', 'comments'</p>
 <p>(dtype='object')</p><br>


```bash
  df.nunique()
```
<img  src="upload/unique.png">



## Ploting image of attribute with it's data :
<img src="upload/self_employed.png"><br>
       
## Boxplot of age attribute :

<img src="upload/plot_image.png">

<br>
<br>

## Filtering the age

```bash
  df.drop(df[df['Age'] < 0].index, inplace = True)
  df.drop(df[df['Age'] > 100].index, inplace = True)
```

<br>
<br>

## Print unique number

```bash
  df['Age'].unique()
```
 
->   [37, 44, 32, 31, 33, 35, 39, 42, 23, 29, 36, 27, 46, 41, 34, 30, 40, 38, 50, 24, 18, 28, 26, 22, 19, 25, 45, 21, 43, 56, 60, 54, 55, 48, 20, 57, 58, 47, 62, 51, 65, 49,  5, 53, 61,  8, 11, 72])

<br>
<br>

## Hisplot figure :
<img src="upload/bar_image.png"><br>

## Unique data :
```bash
  df['Gender'].unique()
```
-> array(['Female', 'Male', 'Other'], dtype=object)<br>

### Attribute Option Count

```python
  df['Gender'].value_counts()
```

| Gender    | Value     |
| :-------- | :-------  | 
| Male    | 988     | 
| Female  | 247     | 
| Other   | 19      |

`Name: Gender, dtype: int64`

<br>

## Figure :
<img src="upload/gender.png"><br>

## Pie chart :
<img src="upload/pie_chart.png"><br>

## Figure of attribute like (self-employed) with treatment :
<img src="upload/self_employed_seeking_treatment.png"><br>

## Heat map :
<img src="upload/heatmap.png"><br>

## Accuracy of all ML algorithm
<!--<ul>
  <li><b>LogisticRegression : </b> 0.7898089171974523<br></li>
  <li><b>KNeighborsClassifier : </b> 0.697452229299363<br></li>
  <li><b>DecisionTreeClassifier : </b> 0.7484076433121019<br></li>
  <li><b>RandomForestClassifier : </b> 0.802547770700637<br></li>
  <li><b>GradientBoostingClassifier : </b> 0.8057324840764332<br></li>
  <li><b>AdaBoostClassifier : </b> 0.7866242038216561<br></li>
  <li><b>XGBClassifier : </b> 0.7961783439490446<br></li>
 </ul>-->
| Algorithm                   | Accuracy Score        |
| :--------                   | :-------              | 
| LogisticRegression          | 0.7898089171974523    | 
| KNeighborsClassifier        | 0.697452229299363     | 
| DecisionTreeClassifier      | 0.7484076433121019    |
| RandomForestClassifier      | 0.802547770700637     |
| GradientBoostingClassifier  | 0.8057324840764332    |
| AdaBoostClassifier          | 0.7866242038216561    |
| XGBClassifier               | 0.7961783439490446    |
 
<br>
<br>

## Data in the figure :
<img src="upload/plotting_the_model_accuracies.png"><br>

<br>
<br>

## Selecting ML having high accuracy :

### The Algorithm which gives maximum accuracy...<br>
### <b>GradientBoostingClassifier : 0.8057324840764332</b>

<br>
<br>

## Confusion matrix of Gradient booster :
<img src="upload/confusion_matrix.png"><br>

<br>
<br>

## ROC curve :
<img src="upload/roc_curve.png">

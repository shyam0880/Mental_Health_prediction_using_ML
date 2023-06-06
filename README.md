# Mental_Health_prediction_using_ML
The project develops a ML solution by implementing multiple algorithms to solve a specific problem. Through rigorous evaluation, the project assesses algorithm performance considering accuracy, speed, and resource requirements. The best algorithm is selected based on optimal results, balancing efficiency and effectiveness.

<p>Data= survey.csv</p>

<p>The dataset contains 1259 rows and 27 columns.</p>
<br>
<b>Dataset column</b>

<p>'Timestamp', 'Age', 'Gender', 'Country', 'state', 'self_employed','family_history', 'treatment', 'work_interfere', 'no_employees','remote_work', 'tech_company', 'benefits', 'care_options','wellness_program', 'seek_help', 'anonymity', 'leave','mental_health_consequence', 'phys_health_consequence', 'coworkers',
 'supervisor', 'mental_health_interview', 'phys_health_interview','mental_vs_physical', 'obs_consequence', 'comments'</p>
 <p>(dtype='object')</p><br>

<img  src="upload/unique.png">



<p><b>#&nbspPloting image of attribute with it's data</b><p>
<img src="upload/self_employed.png"><br>
       
<p><b>#&nbspBoxplot of age attribute</b><p>
<br>

<img src="upload/plot_image.png">

<p><b>#&nbspFiltering the age</b><p>

<p>df.drop(df[df['Age'] < 0].index, inplace = True)<br>
df.drop(df[df['Age'] > 100].index, inplace = True)</p><br>

<p><b>#&nbspPrint unique number</b><p>
df['Age'].unique()<br>
[37, 44, 32, 31, 33, 35, 39, 42, 23, 29, 36, 27, 46, 41, 34, 30, 40, 38, 50, 24, 18, 28, 26, 22, 19, 25, 45, 21, 43, 56, 60, 54, 55, 48, 20, 57, 58, 47, 62, 51, 65, 49,  5, 53, 61,  8, 11, 72])<br>

<p><b>#&nbspHisplot figure</b><p>
<img src="upload/bar_image.png"><br>

<p><b>#&nbspUnique data</b><p>
df['Gender'].unique()<br>
array(['Female', 'Male', 'Other'], dtype=object)<br>

<br>
<img src="upload/gender_data.png"><br>

<p><b>#&nbspFigure</b><p>
<img src="upload/gender.png"><br>

<p><b>#&nbspPie chart</b><p>
<img src="upload/pie_chart.png"><br>

<p><b>#&nbspFigure of attribute like (self employed) with treatement</b><p>
<img src="upload/self_employed_seeking_treatment.png"><br>

<p><b>#&nbspHeat map</b><p>
<img src="upload/heatmap.png"><br>

<p><b>#&nbspAccuracy of all ML algorithm</b><p>
LogisticRegression 0.7898089171974523<br>
KNeighborsClassifier 0.697452229299363<br>
DecisionTreeClassifier 0.7484076433121019<br>
RandomForestClassifier 0.802547770700637<br>
GradientBoostingClassifier 0.8057324840764332<br>
AdaBoostClassifier 0.7866242038216561<br>
XGBClassifier 0.7961783439490446<br>

<p><b>#&nbspData in figure</b><p><br>
<img src="upload/plotting_the_model_accuracies.png"><br>

<p><b>#&nbspSelecting ML having high accuracy</b><p>

The Algorithm which gives maximum accuracy...<br>
GradientBoostingClassifier : 0.8057324840764332

<p><b>#&nbspConfusion matrix of Gradient booster</b><p>
<img src="upload/confusion_matrix.png"><br>

<p><b>#&nbspROC curve</b><p>
<img src="upload/roc_curve.png">

# **TikTok Project**
**Course 2 - Get Started with Python**

Welcome to the TikTok Project!

You have just started as a data professional at TikTok.

The team is still in the early stages of the project. You have received notice that TikTok's leadership team has approved the project proposal. To gain clear insights to prepare for a claims classification model, TikTok's provided data must be examined to begin the process of exploratory data analysis (EDA).

A notebook was structured and prepared to help you in this project. Please complete the following questions.

# **Course 2 End-of-course project: Inspect and analyze data**

In this activity, you will examine data provided and prepare it for analysis.
<br/>

**The purpose** of this project is to investigate and understand the data provided. This activity will:

1.   Acquaint you with the data

2.   Compile summary information about the data

3.   Begin the process of EDA and reveal insights contained in the data

4.   Prepare you for more in-depth EDA, hypothesis testing, and statistical analysis

**The goal** is to construct a dataframe in Python, perform a cursory inspection of the provided dataset, and inform TikTok data team members of your findings.
<br/>
*This activity has three parts:*

**Part 1:** Understand the situation
* How can you best prepare to understand and organize the provided TikTok information?

**Part 2:** Understand the data

* Create a pandas dataframe for data learning and future exploratory data analysis (EDA) and statistical activities

* Compile summary information about the data to inform next steps

**Part 3:** Understand the variables

* Use insights from your examination of the summary data to guide deeper investigation into variables

<br/>

To complete the activity, follow the instructions and answer the questions below. Then, you will us your responses to these questions and the questions included in the Course 2 PACE Strategy Document to create an executive summary.

Be sure to complete this activity before moving on to Course 3. You can assess your work by comparing the results to a completed exemplar after completing the end-of-course project.

# **Identify data types and compile summary information**


Throughout these project notebooks, you'll see references to the problem-solving framework PACE. The following notebook components are labeled with the respective PACE stage: Plan, Analyze, Construct, and Execute.

# **PACE stages**

<img src="images/Pace.png" width="100" height="100" align=left>

   *        [Plan](#scrollTo=psz51YkZVwtN&line=3&uniqifier=1)
   *        [Analyze](#scrollTo=mA7Mz_SnI8km&line=4&uniqifier=1)
   *        [Construct](#scrollTo=Lca9c8XON8lc&line=2&uniqifier=1)
   *        [Execute](#scrollTo=401PgchTPr4E&line=2&uniqifier=1)

<img src="images/Plan.png" width="100" height="100" align=left>


## **PACE: Plan**

Consider the questions in your PACE Strategy Document and those below to craft your response:



### **Task 1. Understand the situation**

*   How can you best prepare to understand and organize the provided information?


*Begin by exploring your dataset and consider reviewing the Data Dictionary.*

Reading the data directory gives me a very good understanding of what the dataset should look like ideally. Also reading the description of the deliverables. And the emails sent to me regarding the project

<img src="images/Analyze.png" width="100" height="100" align=left>

## **PACE: Analyze**

Consider the questions in your PACE Strategy Document to reflect on the Analyze stage.

### **Task 2a. Imports and data loading**

Start by importing the packages that you will need to load and explore the dataset. Make sure to use the following import statements:
*   `import pandas as pd`

*   `import numpy as np`



```python
import pandas as pd
import numpy as np

```


```python
# Load dataset into dataframe
data = pd.read_csv("tiktok_dataset.csv")
```

### **Task 2b. Understand the data - Inspect the data**

View and inspect summary information about the dataframe by **coding the following:**

1. `data.head(10)`
2. `data.info()`
3. `data.describe()`

*Consider the following questions:*

**Question 1:** When reviewing the first few rows of the dataframe, what do you observe about the data? What does each row represent?

**Question 2:** When reviewing the `data.info()` output, what do you notice about the different variables? Are there any null values? Are all of the variables numeric? Does anything else stand out?

**Question 3:** When reviewing the `data.describe()` output, what do you notice about the distributions of each variable? Are there any questionable values? Does it seem that there are outlier values?

















Then, load the dataset into a dataframe. Creating a dataframe will help you conduct data manipulation, exploratory data analysis (EDA), and statistical activities.

**Note:** As shown in this cell, the dataset has been automatically loaded in for you. You do not need to download the .csv file, or provide more code, in order to access the dataset and proceed with this lab. Please continue with this activity by completing the following instructions.


```python
data.head(10)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>#</th>
      <th>claim_status</th>
      <th>video_id</th>
      <th>video_duration_sec</th>
      <th>video_transcription_text</th>
      <th>verified_status</th>
      <th>author_ban_status</th>
      <th>likes_per_view</th>
      <th>comments_per_view</th>
      <th>shares_per_view</th>
      <th>video_view_count</th>
      <th>video_like_count</th>
      <th>video_share_count</th>
      <th>video_download_count</th>
      <th>video_comment_count</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>claim</td>
      <td>7017666017</td>
      <td>59</td>
      <td>someone shared with me that drone deliveries a...</td>
      <td>not verified</td>
      <td>under review</td>
      <td>0.056584</td>
      <td>0.000000</td>
      <td>0.000702</td>
      <td>343296.0</td>
      <td>19425.0</td>
      <td>241.0</td>
      <td>1.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>claim</td>
      <td>4014381136</td>
      <td>32</td>
      <td>someone shared with me that there are more mic...</td>
      <td>not verified</td>
      <td>active</td>
      <td>0.549096</td>
      <td>0.004855</td>
      <td>0.135111</td>
      <td>140877.0</td>
      <td>77355.0</td>
      <td>19034.0</td>
      <td>1161.0</td>
      <td>684.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>claim</td>
      <td>9859838091</td>
      <td>31</td>
      <td>someone shared with me that american industria...</td>
      <td>not verified</td>
      <td>active</td>
      <td>0.108282</td>
      <td>0.000365</td>
      <td>0.003168</td>
      <td>902185.0</td>
      <td>97690.0</td>
      <td>2858.0</td>
      <td>833.0</td>
      <td>329.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>claim</td>
      <td>1866847991</td>
      <td>25</td>
      <td>someone shared with me that the metro of st. p...</td>
      <td>not verified</td>
      <td>active</td>
      <td>0.548459</td>
      <td>0.001335</td>
      <td>0.079569</td>
      <td>437506.0</td>
      <td>239954.0</td>
      <td>34812.0</td>
      <td>1234.0</td>
      <td>584.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>claim</td>
      <td>7105231098</td>
      <td>19</td>
      <td>someone shared with me that the number of busi...</td>
      <td>not verified</td>
      <td>active</td>
      <td>0.622910</td>
      <td>0.002706</td>
      <td>0.073175</td>
      <td>56167.0</td>
      <td>34987.0</td>
      <td>4110.0</td>
      <td>547.0</td>
      <td>152.0</td>
    </tr>
    <tr>
      <th>5</th>
      <td>6</td>
      <td>claim</td>
      <td>8972200955</td>
      <td>35</td>
      <td>someone shared with me that gross domestic pro...</td>
      <td>not verified</td>
      <td>under review</td>
      <td>0.521454</td>
      <td>0.005516</td>
      <td>0.185069</td>
      <td>336647.0</td>
      <td>175546.0</td>
      <td>62303.0</td>
      <td>4293.0</td>
      <td>1857.0</td>
    </tr>
    <tr>
      <th>6</th>
      <td>7</td>
      <td>claim</td>
      <td>4958886992</td>
      <td>16</td>
      <td>someone shared with me that elvis presley has ...</td>
      <td>not verified</td>
      <td>active</td>
      <td>0.647958</td>
      <td>0.007258</td>
      <td>0.258429</td>
      <td>750345.0</td>
      <td>486192.0</td>
      <td>193911.0</td>
      <td>8616.0</td>
      <td>5446.0</td>
    </tr>
    <tr>
      <th>7</th>
      <td>8</td>
      <td>claim</td>
      <td>2270982263</td>
      <td>41</td>
      <td>someone shared with me that the best selling s...</td>
      <td>not verified</td>
      <td>active</td>
      <td>0.001958</td>
      <td>0.000020</td>
      <td>0.000091</td>
      <td>547532.0</td>
      <td>1072.0</td>
      <td>50.0</td>
      <td>22.0</td>
      <td>11.0</td>
    </tr>
    <tr>
      <th>8</th>
      <td>9</td>
      <td>claim</td>
      <td>5235769692</td>
      <td>50</td>
      <td>someone shared with me that about half of the ...</td>
      <td>not verified</td>
      <td>active</td>
      <td>0.409364</td>
      <td>0.001088</td>
      <td>0.042306</td>
      <td>24819.0</td>
      <td>10160.0</td>
      <td>1050.0</td>
      <td>53.0</td>
      <td>27.0</td>
    </tr>
    <tr>
      <th>9</th>
      <td>10</td>
      <td>claim</td>
      <td>4660861094</td>
      <td>45</td>
      <td>someone shared with me that it would take a 50...</td>
      <td>verified</td>
      <td>active</td>
      <td>0.183612</td>
      <td>0.002727</td>
      <td>0.072714</td>
      <td>931587.0</td>
      <td>171051.0</td>
      <td>67739.0</td>
      <td>4104.0</td>
      <td>2540.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
data.info()
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 19382 entries, 0 to 19381
    Data columns (total 15 columns):
     #   Column                    Non-Null Count  Dtype  
    ---  ------                    --------------  -----  
     0   #                         19382 non-null  int64  
     1   claim_status              19084 non-null  object 
     2   video_id                  19382 non-null  int64  
     3   video_duration_sec        19382 non-null  int64  
     4   video_transcription_text  19084 non-null  object 
     5   verified_status           19382 non-null  object 
     6   author_ban_status         19382 non-null  object 
     7   likes_per_view            19084 non-null  float64
     8   comments_per_view         19084 non-null  float64
     9   shares_per_view           19084 non-null  float64
     10  video_view_count          19084 non-null  float64
     11  video_like_count          19084 non-null  float64
     12  video_share_count         19084 non-null  float64
     13  video_download_count      19084 non-null  float64
     14  video_comment_count       19084 non-null  float64
    dtypes: float64(8), int64(3), object(4)
    memory usage: 2.2+ MB



```python
data.describe()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>#</th>
      <th>video_id</th>
      <th>video_duration_sec</th>
      <th>likes_per_view</th>
      <th>comments_per_view</th>
      <th>shares_per_view</th>
      <th>video_view_count</th>
      <th>video_like_count</th>
      <th>video_share_count</th>
      <th>video_download_count</th>
      <th>video_comment_count</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>19382.000000</td>
      <td>1.938200e+04</td>
      <td>19382.000000</td>
      <td>19084.000000</td>
      <td>19084.000000</td>
      <td>19084.000000</td>
      <td>19084.000000</td>
      <td>19084.000000</td>
      <td>19084.000000</td>
      <td>19084.000000</td>
      <td>19084.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>9691.500000</td>
      <td>5.627454e+09</td>
      <td>32.421732</td>
      <td>0.276093</td>
      <td>0.000954</td>
      <td>0.054860</td>
      <td>254708.558688</td>
      <td>84304.636030</td>
      <td>16735.248323</td>
      <td>1049.429627</td>
      <td>349.312146</td>
    </tr>
    <tr>
      <th>std</th>
      <td>5595.245794</td>
      <td>2.536440e+09</td>
      <td>16.229967</td>
      <td>0.173006</td>
      <td>0.001326</td>
      <td>0.050597</td>
      <td>322893.280814</td>
      <td>133420.546814</td>
      <td>32036.174350</td>
      <td>2004.299894</td>
      <td>799.638865</td>
    </tr>
    <tr>
      <th>min</th>
      <td>1.000000</td>
      <td>1.234959e+09</td>
      <td>5.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>20.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>4846.250000</td>
      <td>3.430417e+09</td>
      <td>18.000000</td>
      <td>0.130240</td>
      <td>0.000098</td>
      <td>0.014445</td>
      <td>4942.500000</td>
      <td>810.750000</td>
      <td>115.000000</td>
      <td>7.000000</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>9691.500000</td>
      <td>5.618664e+09</td>
      <td>32.000000</td>
      <td>0.264037</td>
      <td>0.000455</td>
      <td>0.039739</td>
      <td>9954.500000</td>
      <td>3403.500000</td>
      <td>717.000000</td>
      <td>46.000000</td>
      <td>9.000000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>14536.750000</td>
      <td>7.843960e+09</td>
      <td>47.000000</td>
      <td>0.398482</td>
      <td>0.001268</td>
      <td>0.081864</td>
      <td>504327.000000</td>
      <td>125020.000000</td>
      <td>18222.000000</td>
      <td>1156.250000</td>
      <td>292.000000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>19382.000000</td>
      <td>9.999873e+09</td>
      <td>60.000000</td>
      <td>0.666648</td>
      <td>0.010280</td>
      <td>0.265956</td>
      <td>999817.000000</td>
      <td>657830.000000</td>
      <td>256130.000000</td>
      <td>14994.000000</td>
      <td>9599.000000</td>
    </tr>
  </tbody>
</table>
</div>



data.head(10)
The first few lines of data, makes light of few things. All the first five entries are claims. So that would be worth exploring wether theres some sort of bias, or there should be some sort of randomisation or other sorting and filtering. Its also worth noting that the first line has no video_comments, indicating that comments were disabled. There seems to be little correaltion between how many times a video is viewed and shared. 

data.info()
There first apparent observeration is the number of total rows and the non-null values. There seems to be an connection between 298 rows and null values. There is a mix of datatypes, both, ints, floats and objects. Objects for 
"verified_status" and "author_ban_status" could possibly be booleans instead since theyd take less space and memory? The number(#), could do with a more descpitive name, rather than a special character.    

data.describe()
"video_like_count","video_share_count", "video_download_count", "video_comment_count" seems likes columns worth investigating to establish wether the 0 value is a and outlier worth filtering out or they're all relevant. Also the range of values for these fields are very wide, and would also indicate theres something in the date obscuring the view. They also have means that are very close to the 75% percentile, futher implying that the data in the current state is not giving the whole picture

"video_view_count" has an everage of 254708, but the less looking at the quantiles it suggest that a few videos are increasing the average. Is it worth using a median here to compare? 

All the objects are missing due to not being possible to to numerical operatiosn on them. But the 3 of them could be boolean instead, which would make it alot easier to gain insight without compromising the data

### **Task 2c. Understand the data - Investigate the variables**

In this phase, you will begin to investigate the variables more closely to better understand them.

You know from the project proposal that the ultimate objective is to use machine learning to classify videos as either claims or opinions. A good first step towards understanding the data might therefore be examining the `claim_status` variable. Begin by determining how many videos there are for each different claim status.


```python
print(data.groupby("claim_status")["claim_status"].count())
claim_num = (data.groupby("claim_status")["claim_status"].count()) / (data.groupby("claim_status")["claim_status"].count().sum())

print(data.groupby("claim_status")["claim_status"].count().sum())


print((len(data)) == (data.groupby("claim_status")["claim_status"].count().sum()))
print(claim_num * 100)

```

    claim_status
    claim      9608
    opinion    9476
    Name: claim_status, dtype: int64
    19084
    False
    claim_status
    claim      50.345839
    opinion    49.654161
    Name: claim_status, dtype: float64


There are rows missing their claim_status, as previously established. Apart from that, they're very equally split

Next, examine the engagement trends associated with each different claim status.

Start by using Boolean masking to filter the data according to claim status, then calculate the mean and median view counts for each claim status.


```python
mask_claim = data['claim_status'] == "claim"
mask_opinion = data[('claim_status')] == "opinion"



data[mask_opinion]  
data[mask_claim]  
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>#</th>
      <th>claim_status</th>
      <th>video_id</th>
      <th>video_duration_sec</th>
      <th>video_transcription_text</th>
      <th>verified_status</th>
      <th>author_ban_status</th>
      <th>likes_per_view</th>
      <th>comments_per_view</th>
      <th>shares_per_view</th>
      <th>video_view_count</th>
      <th>video_like_count</th>
      <th>video_share_count</th>
      <th>video_download_count</th>
      <th>video_comment_count</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>claim</td>
      <td>7017666017</td>
      <td>59</td>
      <td>someone shared with me that drone deliveries a...</td>
      <td>not verified</td>
      <td>under review</td>
      <td>0.056584</td>
      <td>0.000000</td>
      <td>0.000702</td>
      <td>343296.0</td>
      <td>19425.0</td>
      <td>241.0</td>
      <td>1.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>claim</td>
      <td>4014381136</td>
      <td>32</td>
      <td>someone shared with me that there are more mic...</td>
      <td>not verified</td>
      <td>active</td>
      <td>0.549096</td>
      <td>0.004855</td>
      <td>0.135111</td>
      <td>140877.0</td>
      <td>77355.0</td>
      <td>19034.0</td>
      <td>1161.0</td>
      <td>684.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>claim</td>
      <td>9859838091</td>
      <td>31</td>
      <td>someone shared with me that american industria...</td>
      <td>not verified</td>
      <td>active</td>
      <td>0.108282</td>
      <td>0.000365</td>
      <td>0.003168</td>
      <td>902185.0</td>
      <td>97690.0</td>
      <td>2858.0</td>
      <td>833.0</td>
      <td>329.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>claim</td>
      <td>1866847991</td>
      <td>25</td>
      <td>someone shared with me that the metro of st. p...</td>
      <td>not verified</td>
      <td>active</td>
      <td>0.548459</td>
      <td>0.001335</td>
      <td>0.079569</td>
      <td>437506.0</td>
      <td>239954.0</td>
      <td>34812.0</td>
      <td>1234.0</td>
      <td>584.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>claim</td>
      <td>7105231098</td>
      <td>19</td>
      <td>someone shared with me that the number of busi...</td>
      <td>not verified</td>
      <td>active</td>
      <td>0.622910</td>
      <td>0.002706</td>
      <td>0.073175</td>
      <td>56167.0</td>
      <td>34987.0</td>
      <td>4110.0</td>
      <td>547.0</td>
      <td>152.0</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>9603</th>
      <td>9604</td>
      <td>claim</td>
      <td>3883493316</td>
      <td>49</td>
      <td>a colleague discovered on the radio a claim th...</td>
      <td>not verified</td>
      <td>active</td>
      <td>0.625010</td>
      <td>0.004574</td>
      <td>0.073999</td>
      <td>737177.0</td>
      <td>460743.0</td>
      <td>54550.0</td>
      <td>8119.0</td>
      <td>3372.0</td>
    </tr>
    <tr>
      <th>9604</th>
      <td>9605</td>
      <td>claim</td>
      <td>4765029942</td>
      <td>9</td>
      <td>a colleague discovered on the radio a claim th...</td>
      <td>verified</td>
      <td>active</td>
      <td>0.658297</td>
      <td>0.004446</td>
      <td>0.145060</td>
      <td>546987.0</td>
      <td>360080.0</td>
      <td>79346.0</td>
      <td>4537.0</td>
      <td>2432.0</td>
    </tr>
    <tr>
      <th>9605</th>
      <td>9606</td>
      <td>claim</td>
      <td>3513102998</td>
      <td>27</td>
      <td>a colleague discovered on the radio a claim th...</td>
      <td>not verified</td>
      <td>under review</td>
      <td>0.236556</td>
      <td>0.000897</td>
      <td>0.050011</td>
      <td>885521.0</td>
      <td>209475.0</td>
      <td>44286.0</td>
      <td>1210.0</td>
      <td>794.0</td>
    </tr>
    <tr>
      <th>9606</th>
      <td>9607</td>
      <td>claim</td>
      <td>9461481859</td>
      <td>27</td>
      <td>a colleague discovered on the radio a claim th...</td>
      <td>not verified</td>
      <td>active</td>
      <td>0.278612</td>
      <td>0.001393</td>
      <td>0.058910</td>
      <td>356747.0</td>
      <td>99394.0</td>
      <td>21016.0</td>
      <td>1163.0</td>
      <td>497.0</td>
    </tr>
    <tr>
      <th>9607</th>
      <td>9608</td>
      <td>claim</td>
      <td>1622115206</td>
      <td>16</td>
      <td>a colleague discovered on the radio a claim th...</td>
      <td>not verified</td>
      <td>banned</td>
      <td>0.195480</td>
      <td>0.001627</td>
      <td>0.058388</td>
      <td>114288.0</td>
      <td>22341.0</td>
      <td>6673.0</td>
      <td>284.0</td>
      <td>186.0</td>
    </tr>
  </tbody>
</table>
<p>9608 rows × 15 columns</p>
</div>




```python
# What is the average view count of videos with "opinion" status?

(data[mask_opinion]["video_view_count"]).mean()

data[mask_opinion].describe()
#data[mask_claim].describe()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>#</th>
      <th>video_id</th>
      <th>video_duration_sec</th>
      <th>likes_per_view</th>
      <th>video_view_count</th>
      <th>video_like_count</th>
      <th>video_share_count</th>
      <th>video_download_count</th>
      <th>video_comment_count</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>9476.000000</td>
      <td>9.476000e+03</td>
      <td>9476.000000</td>
      <td>0.0</td>
      <td>9476.000000</td>
      <td>9476.000000</td>
      <td>9476.000000</td>
      <td>9476.000000</td>
      <td>9476.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>14346.500000</td>
      <td>5.622382e+09</td>
      <td>32.359856</td>
      <td>NaN</td>
      <td>4956.432250</td>
      <td>1092.729844</td>
      <td>217.145631</td>
      <td>13.677290</td>
      <td>2.697446</td>
    </tr>
    <tr>
      <th>std</th>
      <td>2735.629909</td>
      <td>2.530209e+09</td>
      <td>16.281705</td>
      <td>NaN</td>
      <td>2885.907219</td>
      <td>964.099816</td>
      <td>252.269583</td>
      <td>16.200652</td>
      <td>4.089288</td>
    </tr>
    <tr>
      <th>min</th>
      <td>9609.000000</td>
      <td>1.234959e+09</td>
      <td>5.000000</td>
      <td>NaN</td>
      <td>20.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>11977.750000</td>
      <td>3.448802e+09</td>
      <td>18.000000</td>
      <td>NaN</td>
      <td>2467.000000</td>
      <td>289.000000</td>
      <td>34.000000</td>
      <td>2.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>14346.500000</td>
      <td>5.611857e+09</td>
      <td>32.000000</td>
      <td>NaN</td>
      <td>4953.000000</td>
      <td>823.000000</td>
      <td>121.000000</td>
      <td>7.000000</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>16715.250000</td>
      <td>7.853243e+09</td>
      <td>47.000000</td>
      <td>NaN</td>
      <td>7447.250000</td>
      <td>1664.000000</td>
      <td>314.000000</td>
      <td>19.000000</td>
      <td>3.000000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>19084.000000</td>
      <td>9.999835e+09</td>
      <td>60.000000</td>
      <td>NaN</td>
      <td>9998.000000</td>
      <td>4375.000000</td>
      <td>1674.000000</td>
      <td>101.000000</td>
      <td>32.000000</td>
    </tr>
  </tbody>
</table>
</div>



**Question:** What do you notice about the mean and media within each claim category?
The average views are much higher for opinions than claims 501029 vs 4956

Now, examine trends associated with the ban status of the author.

Use `groupby()` to calculate how many videos there are for each combination of categories of claim status and author ban status.


```python
data.groupby(['claim_status','author_ban_status'])['video_id'].count()

```




    claim_status  author_ban_status
    claim         active               6566
                  banned               1439
                  under review         1603
    opinion       active               8817
                  banned                196
                  under review          463
    Name: video_id, dtype: int64



**Question:** What do you notice about the number of claims videos with banned authors? Why might this relationship occur?

The claims category have much higher numbers in the category of banned and under review. They also have lower number of active users. 


Continue investigating engagement levels, now focusing on `author_ban_status`.

Calculate the median video share count of each author ban status.


```python

```


```python
# What's the median video share count of each author ban status?
data.groupby(['author_ban_status'])['video_share_count'].median()
```




    author_ban_status
    active            437.0
    banned          14468.0
    under review     9444.0
    Name: video_share_count, dtype: float64



**Question:** What do you notice about the share count of banned authors, compared to that of active authors? Explore this in more depth.

The median video_share_count is much higher for banned users than active users.

Use `groupby()` to group the data by `author_ban_status`, then use `agg()` to get the count, mean, and median of each of the following columns:
* `video_view_count`
* `video_like_count`
* `video_share_count`

Remember, the argument for the `agg()` function is a dictionary whose keys are columns. The values for each column are a list of the calculations you want to perform.


```python
data.groupby(['author_ban_status'])["video_view_count","video_like_count","video_share_count"].agg(['count', 'mean', 'median'])
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead tr th {
        text-align: left;
    }

    .dataframe thead tr:last-of-type th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr>
      <th></th>
      <th colspan="3" halign="left">video_view_count</th>
      <th colspan="3" halign="left">video_like_count</th>
      <th colspan="3" halign="left">video_share_count</th>
    </tr>
    <tr>
      <th></th>
      <th>count</th>
      <th>mean</th>
      <th>median</th>
      <th>count</th>
      <th>mean</th>
      <th>median</th>
      <th>count</th>
      <th>mean</th>
      <th>median</th>
    </tr>
    <tr>
      <th>author_ban_status</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>active</th>
      <td>15383</td>
      <td>215927.039524</td>
      <td>8616.0</td>
      <td>15383</td>
      <td>71036.533836</td>
      <td>2222.0</td>
      <td>15383</td>
      <td>14111.466164</td>
      <td>437.0</td>
    </tr>
    <tr>
      <th>banned</th>
      <td>1635</td>
      <td>445845.439144</td>
      <td>448201.0</td>
      <td>1635</td>
      <td>153017.236697</td>
      <td>105573.0</td>
      <td>1635</td>
      <td>29998.942508</td>
      <td>14468.0</td>
    </tr>
    <tr>
      <th>under review</th>
      <td>2066</td>
      <td>392204.836399</td>
      <td>365245.5</td>
      <td>2066</td>
      <td>128718.050339</td>
      <td>71204.5</td>
      <td>2066</td>
      <td>25774.696999</td>
      <td>9444.0</td>
    </tr>
  </tbody>
</table>
</div>



**Question:** What do you notice about the number of views, likes, and shares for banned authors compared to active authors?
Banned users are more popular in view_count, like_count and video_share. Almost by double compared to active ones. Even the under review status, is more popular than the active ones. but by average and median.

Now, create three new columns to help better understand engagement rates:
* `likes_per_view`: represents the number of likes divided by the number of views for each video
* `comments_per_view`: represents the number of comments divided by the number of views for each video
* `shares_per_view`: represents the number of shares divided by the number of views for each video


```python
# Create a likes_per_view column
data.insert(7,"likes_per_view",(data['video_like_count'] / data['video_view_count']))

# Create a comments_per_view column
data.insert(8,"comments_per_view",(data['video_comment_count'] / data['video_view_count']))

# Create a shares_per_view column
data.insert(9,"shares_per_view",(data['video_share_count'] / data['video_view_count']))
```


    ---------------------------------------------------------------------------

    ValueError                                Traceback (most recent call last)

    <ipython-input-6-5c8583dd377e> in <module>
          1 # Create a likes_per_view column
    ----> 2 data.insert(7,"likes_per_view",(data['video_like_count'] / data['video_view_count']))
          3 
          4 # Create a comments_per_view column
          5 data.insert(8,"comments_per_view",(data['video_comment_count'] / data['video_view_count']))


    /opt/conda/lib/python3.7/site-packages/pandas/core/frame.py in insert(self, loc, column, value, allow_duplicates)
       4412         if not allow_duplicates and column in self.columns:
       4413             # Should this be a different kind of error??
    -> 4414             raise ValueError(f"cannot insert {column}, already exists")
       4415         if not isinstance(loc, int):
       4416             raise TypeError("loc must be int")


    ValueError: cannot insert likes_per_view, already exists


Use `groupby()` to compile the information in each of the three newly created columns for each combination of categories of claim status and author ban status, then use `agg()` to calculate the count, the mean, and the median of each group.


```python

data.groupby(['claim_status','author_ban_status'])['comments_per_view',"likes_per_view","shares_per_view"].agg(['median','mean','count'])
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead tr th {
        text-align: left;
    }

    .dataframe thead tr:last-of-type th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr>
      <th></th>
      <th></th>
      <th colspan="3" halign="left">comments_per_view</th>
      <th colspan="3" halign="left">likes_per_view</th>
      <th colspan="3" halign="left">shares_per_view</th>
    </tr>
    <tr>
      <th></th>
      <th></th>
      <th>median</th>
      <th>mean</th>
      <th>count</th>
      <th>median</th>
      <th>mean</th>
      <th>count</th>
      <th>median</th>
      <th>mean</th>
      <th>count</th>
    </tr>
    <tr>
      <th>claim_status</th>
      <th>author_ban_status</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th rowspan="3" valign="top">claim</th>
      <th>active</th>
      <td>0.000776</td>
      <td>0.001393</td>
      <td>6566</td>
      <td>0.326538</td>
      <td>0.329542</td>
      <td>6566</td>
      <td>0.049279</td>
      <td>0.065456</td>
      <td>6566</td>
    </tr>
    <tr>
      <th>banned</th>
      <td>0.000746</td>
      <td>0.001377</td>
      <td>1439</td>
      <td>0.358909</td>
      <td>0.345071</td>
      <td>1439</td>
      <td>0.051606</td>
      <td>0.067893</td>
      <td>1439</td>
    </tr>
    <tr>
      <th>under review</th>
      <td>0.000789</td>
      <td>0.001367</td>
      <td>1603</td>
      <td>0.320867</td>
      <td>0.327997</td>
      <td>1603</td>
      <td>0.049967</td>
      <td>0.065733</td>
      <td>1603</td>
    </tr>
    <tr>
      <th rowspan="3" valign="top">opinion</th>
      <th>active</th>
      <td>0.000252</td>
      <td>0.000517</td>
      <td>8817</td>
      <td>0.218330</td>
      <td>0.219744</td>
      <td>8817</td>
      <td>0.032405</td>
      <td>0.043729</td>
      <td>8817</td>
    </tr>
    <tr>
      <th>banned</th>
      <td>0.000193</td>
      <td>0.000434</td>
      <td>196</td>
      <td>0.198483</td>
      <td>0.206868</td>
      <td>196</td>
      <td>0.030728</td>
      <td>0.040531</td>
      <td>196</td>
    </tr>
    <tr>
      <th>under review</th>
      <td>0.000293</td>
      <td>0.000536</td>
      <td>463</td>
      <td>0.228051</td>
      <td>0.226394</td>
      <td>463</td>
      <td>0.035027</td>
      <td>0.044472</td>
      <td>463</td>
    </tr>
  </tbody>
</table>
</div>



**Question:**

How does the data for claim videos and opinion videos compare or differ? Consider views, comments, likes, and shares.
Claim videos generate more response from the audience. Both in terms sharing, likes and comments. 

<img src="images/Construct.png" width="100" height="100" align=left>

## **PACE: Construct**

**Note**: The Construct stage does not apply to this workflow. The PACE framework can be adapted to fit the specific requirements of any project.




<img src="images/Execute.png" width="100" height="100" align=left>

## **PACE: Execute**

Consider the questions in your PACE Strategy Document and those below to craft your response.

### **Given your efforts, what can you summarize for Rosie Mae Bradshaw and the TikTok data team?**

*Note for Learners: Your answer should address TikTok's request for a summary that covers the following points:*

*   What percentage of the data is comprised of claims and what percentage is comprised of opinions?
    
*   What factors correlate with a video's claim status?

*   What factors correlate with a video's engagement level?


The percentage of claim 50.34 % and opinion 49.65%



What what seems to be a correlation in the video's engagement is the notoriety. The Claims that come from users that have been banned or are under reviewd, seem to be causing a lot of user generated traffic, shares, likes and comments.




**Congratulations!** You've completed this lab. However, you may not notice a green check mark next to this item on Coursera's platform. Please continue your progress regardless of the check mark. Just click on the "save" icon at the top of this notebook to ensure your work has been logged.

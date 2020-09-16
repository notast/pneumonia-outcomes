# pneumonia-outcomes
The aim of this project is to classify if patients with Community Acquired Pneumonia (CAP) became better after seeing a doctor or became worse despite seeing a doctor. The [dataset](https://datadryad.org/stash/dataset/doi:10.5061/dryad.r282vk6) is from a [prospective population-based surveillance study](https://bmjopen.bmj.com/content/8/4/e019439.long). The dataset has a wealth of variables which can be used for predictive modelling, there is no known predictive analysis published using this dataset. 
This project was part of an assignment which the aim of the assignment was to use `DataRobot` for predictive modelling. Exploratory data analysis and feature engineering was donein `R` before the data was imported into `DataRobot`.
## Dataset
The dataset consists of 2302 rows and 176 columns. The columns can be grouped into 13 categories. I have appended the metadata to sheet 2 (metadata) and a description of each category to sheet 3 (Category) of the spreadsheet. [More details of the dataset can be found here](https://notast.netlify.app/post/predicting-pneumonia-outcomes-eda-part-1/).
## EDA
[EDA for the first 8 categories can be found here](https://notast.netlify.app/post/predicting-pneumonia-outcomes-eda-part-1/#to-be-continued.). The output is saved as CAP_EDA1.RData 

![](https://github.com/notast/pneumonia-outcomes/blob/master/images/PE%20temp.png)

<br>
[EDA for the 9th to 13th categories can be found here](https://notast.netlify.app/post/predicting-pneumonia-outcomes-eda-part-2/). The output is saved as CAP_EDA12.RData. 
<br>
After EDA and data wrangling the dataset has 2112 rows and 78 columns. 
## Feature Engineering
[Feature engineering was done to futher condense variables and also create a few new variables](https://notast.netlify.app/post/predicting-pneumonia-outcomes-feature-engineering/) After feature engineering, the dataset has 2112 rows and 71 variables.
## DataRobot
To be completed... showing how to use R API for DataRobot and use R to further enhance the DataRobot's performance.

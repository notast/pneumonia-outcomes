# pneumonia-outcomes
The aim of this project is to classify if patients with Community Acquired Pneumonia (CAP) became better after seeing a doctor or became worse despite seeing a doctor. The [dataset](https://datadryad.org/stash/dataset/doi:10.5061/dryad.r282vk6) is from a [prospective population-based surveillance study](https://bmjopen.bmj.com/content/8/4/e019439.long). The dataset has a wealth of variables which can be used for predictive modelling, there is no known predictive analysis published using this dataset. 
This project was part of an assignment which the aim of the assignment was to use `DataRobot` for predictive modelling. Exploratory data analysis and feature engineering was donein `R` before the data was imported into `DataRobot`.
## Dataset
The dataset consists of 2302 rows and 176 columns. The columns can be grouped into 13 categories. 
| #  | Category                        | Category description                                                   | Examples                                                              | Prefix  |
|----|---------------------------------|------------------------------------------------------------------------|-----------------------------------------------------------------------|---------|
| 1  | Patient                         | Variables related to patient details                                   | Case number, age                                                      | Pt_     |
| 2  | Radiology                       | Variables related to medical imaging                                   | Findings on the chest x-ray                                           | R_      |
| 3  | Signs and symptoms              | Signs and symptoms to diagnose CAP.                                    | Did patient have a fever?                                             | SS_     |
| 4  | Medical history                 | Patientís medical history                                              | Did patient have HIV?                                                 | Hx_     |
| 5  | Social history                  | Patientís social history                                               | Did patient smoke?                                                    | Social_ |
| 6  | Healthcare associated pneumonia | Risk factors for healthcare associated pneumonia                       | Was patient previously admitted?                                      | HCAP_   |
| 7  | Physical examination            | Observations during physical examination                               | Was patient confused?                                                 | PE_     |
| 8  | Lab findings                    | Laboratory findings (blood test) closest to the diagnosis of CAP       | Was blood sugar levels tested?, What was the blood sugar level?       | Lab_    |
| 9  | Cultures                        | Mediums used to identify the bug causing the CAP and the bug detected. | Was a urine sample taken? Was the bug detected in patientís phlegm?   | CS_     |
| 10 | Antibiotics                     | Antibiotics prescribed for CAP                                         | Was antibiotic XXX prescribed?                                        | Abx_    |
| 11 | Continuum of care               | Status of the type and extent of care patient received                 | Was the patient admitted? The number of days lost to CAP              | Care_   |
| 12 | Other                           | Other variables                                                        | The outcome. If patient became better or worse after seeing a doctor. | Other_  |
| 13 | Vaccine                         | Vaccines patient received                                              | Did patient have a flu vaccine?                                       | V_      |


I have appended the metadata to sheet 2 (metadata) and a description of each category to sheet 3 (Category) of the spreadsheet. [More details of the dataset can be found here](https://notast.netlify.app/post/predicting-pneumonia-outcomes-eda-part-1/).
## EDA
[EDA for the first 8 categories can be found here](https://notast.netlify.app/post/predicting-pneumonia-outcomes-eda-part-1/#to-be-continued.). 
<img src="https://github.com/notast/pneumonia-outcomes/blob/master/images/PE%20temp.png" alt="" width="900"/>
\
[EDA for the 9th to 13th categories can be found here](https://notast.netlify.app/post/predicting-pneumonia-outcomes-eda-part-2/). 
\
After EDA and data wrangling the dataset has 2112 rows and 78 columns. 
## Feature Engineering
[Feature engineering was done to futher condense variables and also create a few new variables](https://notast.netlify.app/post/predicting-pneumonia-outcomes-feature-engineering/). 
<img src="https://github.com/notast/pneumonia-outcomes/blob/master/images/Lump%20abx.png" alt="" width="1000"/>
<br>
After feature engineering, the dataset has 2112 rows and 71 variables.
## DataRobot
The cleaned up dataset was imported into `DataRobot` for basic modelling. The [results from the first round of modelling were used for advanced feature selection via the `R` API](https://notast.netlify.app/post/predicting-pneumonia-outcomes-modelling-via-datarobot-api/). A smaller but possibly more influential subset of variables were used in a second round of modelling.

<img src="https://notast.netlify.app/post/2020-09-12-predicting-pneumonia-outcomes-modelling-via-datarobot-api_files/figure-html/unnamed-chunk-17-1.png" alt="" width="600"/>
<br>
to be cont.... results after 2 runs of modelling in DataRobot 

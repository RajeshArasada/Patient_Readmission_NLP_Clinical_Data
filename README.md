# Predicting Patient Readmission using Discharge Summaries

[![N|Solid](https://cldup.com/dTxpPi9lDf.thumb.png)](https://nodesource.com/products/nsolid)

[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)

```
Domain 		  : Machine Learning, Natural Language Processing
Techniques	  : Classification techinques
Application	  : Healthcare Management
```

## Dataset Details
Original Dataset		: [MIMIC-III](https://mimic.physionet.org/)
```
Dataset Name              : Medical Information Mart for Intensive Care III(MIMIC-III) hospital database
Dataset                   : de-identified information from over 40,000 patients admitted to 
                            Beth Israel Deaconess Medical Center in Boston, Massachusetts from 
                            2001 to 2012
Tables Used               : Admissions and NoteEvents
Number of Class           : 2
Number of Instances       : 37812 (after data cleaning)
Number of Attributes      : 1 (Discharge summaries)
```
## Problem Definition
A hospital readmission is when a patient who is discharged from the hospital gets re-admitted again within a certain period of time. Readmission of patients is a huge financial burden on the insurance companies and other payment agencies. The hospitals also suffer because it reflects poorly on the quality of the service they provide. Determining factors that lead to higher readmission, and correspondingly being able to predict which patients will get readmitted can help hospitals save millions of dollars while improving quality of care.

In this project I built models predicting readmission to ED (Emergency Departments) for patients using their most recent discharge summaries. The steps I will go through are:
    • data exploration and data cleaning
    • building training/validation/test samples
    • model selection
    • model evaluation
Note that higher sensitivity (recall) is more desirable for hospitals because it is more crucial to correctly identify "high risk" patients who are likely to be readmitted than identifying "low risk" patients.


## Tools/ Libraries
```
Languages     : Python
Tools/IDE     : Jupyter Notebook
Libraries     : Scikit Learn, Pandas, Numpy, Matplotlib, NLTK
```
## Performance Metrics on Validation Data
| | Random Forest  |	Gradient Boosting Machine |
| ------ | -------------- |-------------------------- |
| Accuracy | 0.64 |	0.57 |
| Precision | 0.63 | 0.56 |
| Recall | 0.67	| 0.61 |
| AUC-ROC |	0.64 |	0.57 |

## Conclusions
Through this project, I created a binary classifier to predict the probability that a patient discharged from Emergency Department would be readmitted to the hospital within 30 days. On held out data, my best model was Random Forest with AUC 0.64, Precision 0.63 and Recall 0.67.

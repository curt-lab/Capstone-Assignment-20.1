# Capstone-Assignment-20.1
Initial Report and Exploratory Data Analysis (EDA) 
The contents and charts in this report are also expressed throughout the comments of the accompanying jupyter notebook file.
The task was perform EDA on the datasets identified for my capstone project.

BUSINESS PROBLEM: 
The problem I had identified and discussed with my advisor was to develop a predictive model that would answer the question:
"How would this (red) wine score based on it's properties and characteristics?", and a secondary question (if possible) would be:
"How well would it do in competition?"

DATASETS:
I have looked at lots of potential datasets to see how I might go about answering this question.  I found a particularly useful 
dataset in UCI Machine Learning Repository (https://archive.ics.uci.edu/dataset/186/wine+quality).  There is two datasets-- one 
for white vinho verde wine and one for red vinho verde wine.  While there are more samples in the white wine, my interest is geared 
towards the red wine, which also seems to have greater complexity based on the two heat maps (see attached files) of features for each.
Also, my goal is to develop a model based on this dataset that might be applied to other red wines to estimate their scoring.  The 
challenge has been find any datasets from major wine competitions that provide sufficient data on the measured properties and characteristics
of wines.  The same is true with published experts ratings of wines; for example Robert Parker or James Suckling (two very well-known critics)
rate a wine as "92/100" and describe some arbitrary tasting notes but not detailed information on the wine and it's properties. Perhaps 
with some additional data-scraping I can build such a dataset for the final project.  I will at least try to see if it is possible.  For now,
I do have this good dataset from UCI to use.  In the accompanying jupyter notebook, I have stepped through examining the data and taking steps 
to ensure it is complete and clean.  I also, put the dataset through heatmaps to get some feel for which features were the most influential
toward the quality score.

INITIAL (BASELINE) MODELING (SEE JUPYTER NOTEBOOK):
The way I planned to tackle the primary and secondary question was through a combination of linear regression and classification modeling.  In my
thinking I felt the primary question about scoring with the particular dataset could certainly be answered by using linear regression techniques, 
but also could be viewed as a classification problem where each class is one of the ratings (1-9, with 9 being best quality).  So, in my 
preliminary modeling I started with a simple degree 1 linear regression model and then a degree 2 model.  I also was curious to see what the 
models would reveal as to the most influential (best) features for modeling using GridSearchCV and SFS (Sequential Feature Selection).  It turned out


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
that there were 7 of 11 features that provided the best -MSE score for the degree 1 model.  For the degree 2 model there were only 4 features that 
provided the best -MSE score and only 3 of those are physical properties (one feature being the square of a physical property).  The two -MSE scores 
were nearly the same.  So potentially I could have a model that is reasonably good with only 4 of 11 physical properties of the wine.  That could 
be useful for extending the model to other red wines beyond this dataset.  I also, intend to do more testing with the linear regression models to see how they perform with L1 and L2 regularization models.  

I also did some initial exploration of how a classification model would perform on the same dataset.  Just to get started I tried a decision tree and a logistic regression model just using default pararmeters.  The results were great, with only 59% and 57% accuracy.  Which is better than a wild guess (1 out of 9, or 11%), but I will do deeper exploration of this by GridSearch over a range of hyperparameters.  

CONCLUSIONS:
I have a solid set of data to build the type of predictive model that I wanted to some meaningful degree.  It was great to be see how the various features infuence the quality (outcome) and which faetures matter the most.  I will need to work on finding some addtional datasets to more broadly apply the model to provide a more general answer to the business question.  I am not sure if it will be possible to answer the secondary question, but perhaps with some creative data-scaping and data transformation techniques I can come up with something that will work nicely.  I will put a lot of effort into that so I can review it with my advisor in our second 1:1 session in a couple of weeks.

As far as models go, I will need to work on the trying some additonal modeling such as L1 and L2 for linear regression and SVM and KNN for classification; also testing hyperparameters for classification models more extensively.  I will also need to see how bagging and boosting might fit in with this effort to improve the models.



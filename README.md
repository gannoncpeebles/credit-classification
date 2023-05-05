# Credit Classification

I downloaded a CSV that contained roughly one thousand entries of individuals. It contained data surrounding their
employment, property magnitude, number of dependents, etc.

Using this data set, I tried implementing some machine learning models and then realized that some were not
the proper models for the situaton. At first, I used K-Nearest Neighbors from SciKit-Learn but ran into some issues
regarding trying to scale the training, testing, and validation data sets. To solve this, I simply converted the 
categorical data into quantitative variables (such as 1, 2, 3, etc.) Theoretically, this does not propose any issues
as long as the quantitative assignment is standard for all entries. The reason is because the Euclidian distance will
be standardized when the KNN model is ran (regardless of the weights of each categorical variable.) Essentially, the 
multi-dimensionality will solve the issue. However, I unfortunately forgot to save my work. After realizing this, I
set out to try a new method that did not need as much manipulation/pre-proceessing of the data. I arrived at
KPrototype because it can take in quantitative variables and will use match-making for the
categorical variables to create clusters. I set the clusters equal to 2 because we know the credit will be
good or bad, per the CSV data we took in. I then calculated the accuracy by simpling comparing the clusters
assigned and the actual credit type. I got an accuracy of around 67% on repeated trials. This is actually a pretty
good estimator because our data set was relatively small (only around a thousand entries, rather than a million+) and
the categorical variables were relatively sparse.

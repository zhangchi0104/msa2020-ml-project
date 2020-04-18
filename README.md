# Parkinsons Analysis

## Step 1 - Visuallising Data 
My first step is to visuallise data to obtain some basic ideas about how parkinsons is related to the data in the dataset.
Since the data is clean, I have no need to clean the data. I relate parkinsons to the data in following fields::
	- Vocal Fundimental Frequency
	- Variation in fundamental frequnecy
	- Variation in sound frequnecy
	- noise to total components in voice

By using `matplotlib`, I created several plots in the notbook, Conclusions are also included in the file

## Step 2 Selecting Models

First, by reading through `parkinsons.name` file, I noticed the following
> RPDE,D2 - Two nonlinear dynamical complexity measures
> spread1,spread2,PPE - Three nonlinear measures of fundamental frequency variation

hence linear regression models might not be approiate for this problem. Identifying parkinsons is a classification problem. So using SVM might be a good choice, I will also give logstic regression a go as it  also works for classification problem.



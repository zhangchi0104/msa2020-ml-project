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

## Step X Potential Applications

This model does only one simple thing -- **Predict parkinsons**. It sounds a bit boring. However from the dataset, we noticed that  voice data is used to predict parkinsons. That means any smart devices that can collect and process voice could use this model to predict whether the user has parkinsons or not.

For example, If the model determines the wearer has high probability to get parkinsons. It can warn the wearer and his/her emergency contacts. Even can contact for medical support. 

Such device can be very small. such as smart watch or wrist band, wireless earbuds and hearing aid devices. I believe in the near future, Because of 5G and IoT, These devices will be empowered by these new techs and can be more accurate. For example, smart devices that have less computing power can send data to the cloud server to do the prediction as the server has a constantly envolving model, 

## TODO List
	- [] use a larger dataset
	- [] tone the SVM model

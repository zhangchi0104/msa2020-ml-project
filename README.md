
# Parkinsons Analysis
## Setup
### Azure Notebooks
Open this project straightaway in azure notebooks
### Anaconda
Just open up `parkinsons.ipynb` in jupyter

### Miniconda 
```bash
conda create --name parkinsons --file requirements.txt
```

### VS Code + docker
1. install the `ms-vscode-remote.vscode-remote-extensionpack` from extension market place
2. select the remote development icon from the side pannel
3. select reopen in container


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

## Step 3 Assessing and Toning Models
I examined both models from 3 aspects:
	- mean score
	- ROC AUC score
	- Confusion matrix
Before toning the models, I found the accuracy of the SVM is not as good as I expected, as I believe SVM is more suitable for this problem. 

I tried using different kernels for the SVM model and then toned other parameters for the polynomial kernel. It turned out beating the logistic regression model.

## Step 4 Potential Applications

This model does only one simple thing -- **Predict parkinsons**. It sounds a bit boring. However the advantage of this model is that it uses speech data to predict parkinsons That means any smart devices that can collect and process voice could use this model to predict whether the user has parkinsons or not.

For example, If the model determines the wearer has high probability to get parkinsons. It can warn the wearer and his/her emergency contacts. Even can contact for medical support. 

Such device can be very small. such as smart watch or wrist band, wireless earbuds and hearing aid devices. I believe in the near future, Because of population of 5G and IoT, The form factors of these devices can be much more smaller and more power efficient as models are stored in the cloud. 


# Data Version Controll DVC


## Data: (directory: data/wine_sample.csv) dataset that will be store in S3

fixed_acidity,volatile_acidity,citric_acid,residual_sugar,chlorides,quality
7.4,0.7,0,1.9,0.076,5
7.8,0.88,0,2.6,0.098,5
7.3,0.76,0.04,2.3,0.092.6
7.5,0.65,0.02,2.1,0.075,5
7.2,0.64,0.03,2,0.072,6
7.0,0.62,0.25,6.4,0.065,7
6.8,0.6,0.3,6,0.067,6
7.1,0.58,0.22,5.8,0.07,6
7.6,0.7,0.01,2.4,0.08,5
7.9,0.75,0.04,2.5,0.086,6

======
git init

## initialize dvc

dvc init

## creat data reference file with dvc that will be store in github repo

dvc add data/wine_sample.csv

## Create a S3 bucket in AWS cloud

bucket_name: mlops-xxx

## Add th data in the bucket use dvc

dvc remote add -d wineremote s3://xxx



## config aws to push the data in s3 bucket

aws configure

## push the data

dvc push 


# Experiment Tracking

- It is a process of recording evrything that data scientists do as part of the training process.

- Usually, they do multiple experiments because they don't reach the required efficiency in the very first experiment.

# MLflow

- use for experiment tracking
- version controlle
- deploy



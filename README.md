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

```sh
git init

```

## initialize dvc

```sh
dvc init
```

## creat data reference file with dvc that will be store in github repo

```sh
dvc add data/wine_sample.csv
```

## Create a S3 bucket in AWS cloud

bucket_name: mlops-xxx

## Add th data in the bucket use dvc

```sh
dvc remote add -d wineremote s3://xxx
```

## config aws to push the data in s3 bucket

```sh
aws configure
```

## push the data

```sh
dvc push 
```

# Experiment Tracking

- It is a process of recording evrything that data scientists do as part of the training process.

- Usually, they do multiple experiments because they don't reach the required efficiency in the very first experiment.

# MLflow

- use for experiment tracking
- version controlle
- deploy


====
## connect to mlflow

```sh
# create connection directory:

mkdir mlflow-connect
cd mlflow-connect

# install python env

python3 -n venv .venv

# activate python env

. .venv/bin/activate

# install mlflow python module

python3 -m pip install mlflow

# import mlflow module
python3

import mlflow

# connect to mlflow

mlflow.set_tracking_uri("http://localhost:7006")
mlflow.set_experiment("my-first-experiment-mlflow")
```

## Train the model


```sh
# Install the the requirement

python3 -m pip install -r requirements.txt

# Run train model py

python3 train.py

```




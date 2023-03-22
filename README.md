<h1 align=center> MLOps (Banking Project)</h1>

**Des:** Using DVC and Mlflow 


## Steps

* Create an environment and acitvate it
```bash
conda create -n banking python=3.7 ipykernel -y
conda activate banking
```

* create req file and install it
```bash
touch requirements.txt
pip install -r requirements.txt
```

* [Get the dataset](https://www.kaggle.com/datasets/krantiswalke/bankfullcsv)

```bash
dvc init
```

* adding data into dvc for tracking
```bash
dvc add banking.csv
```

* Add remote storage
```bash
dvc remote add -d storage gdrive://<DRIVE ID>
```

* Push the data to the remote storage
```bash
dvc push
```

* push the changes to github
```bash
git add . && git commit -m "env created, req file added, got the dataset and start tracking data"
git push origin main
```

* create a jupyter notebook
    * Model section
        * **create functions**
        * load the data
        * EDA
        * feature engineering
        * Basic model creatin and making the prediction
    * MLflow Section
        * MLflow experiment creation
        * MLflow creating experiment and register mode
        
        
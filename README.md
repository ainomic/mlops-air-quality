# MLOps on Air Quality Dataset

MLOps end-to-end project on air quality dataset from [OpenAQ](https://openaq.org/) platform.

## Getting started

### File structure

```markdown
project/  
├── dags/  
├── ├── __init__.py  
├── └── data_collection.py  
├── preprocessing/  
├── ├── __init__.py  
├── └── preprocessing_script.py  
├── models/  
├── ├── __init__.py  
├── └── model.py  
├── deployment/  
├── ├── __init__.py  
├── └── app.py  
├── └── templates/  
├── └── ├── index.html  
├── └── └── ...  
└── config.py  
```

__Explanation of the file structure__:

- __dags/__  
  This folder contains Apache Airflow DAGs (Directed Acyclic Graphs) for defining and managing your data collection tasks and workflows. We have created a Python file, `data_collection.py`, within this folder to define our DAGs and their associated tasks.
- __preprocessing/__  
  This folder houses the scripts and modules related to data preprocessing. We have created a Python file, `preprocessing_script.py`, within this folder to write our data preprocessing logic.
- __models/__  
  This folder is dedicated to storing scripts and modules related to our machine learning models. We have created a Python file, `model.py`, within this folder to define and train our models.
- __deployment/__  
  This folder contains the necessary files for deploying our model as a web application. It includes an `app.py` file, which serves as the entry point for our web application, and a `templates/` folder for storing HTML templates and other assets.
- __config.py__  
  This file can hold project-specific configuration settings, such as API keys, database credentials, or any other global parameters used throughout our project. It helps centralize the configuration details for easy access and modification.

### Setup dev environment

1. Create virtual environment: `conda create -n mlops-aq-env -y python=3.8`
1. Activate virtual environment: `conda activate mlops-aq-env`
1. Install Apache Airflow: `./apache_airflow_install.sh`
1. Install requirements: `pip install -r requirements.txt`
1. You're good to go!

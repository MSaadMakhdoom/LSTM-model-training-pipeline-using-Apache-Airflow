# LSTM-model-training-pipeline-using-Apache-Airflow
Apache Airflow  used to automate the training and deployment of LSTM models. In this tutorial, Build an LSTM model training pipeline using Apache Airflow. The pipeline will automate the following steps: 
* Data preprocessing  
* Model training 
* Model evaluation
# Setup Apache Airflow
# create virtual environment
```
conda create --name airflow_env python=3.9
```
# To activate this environment
```
conda activate airflow_env
```
# To deactivate an active environment
```
conda deactivate
```
 # install Apache Airflow:
 ```
pip install "apache-airflow==2.2.3" --constraint "https://raw.githubusercontent.com/apache/airflow/constraints-2.2.3/constraints-no-providers-3.9.txt"
```

# initialize the database
```
airflow db init
```

# Create an admin account:

```
airflow users create --username msaad --firstname Muhammad --lastname Saad --email msaadmakhdoom@gmail.com --role Admin --password 123456
```
# airflow folder in your root directory, so navigate to it:
```
cd ~/airflow
```

# First, start the Webserver in the daemon mode
```
airflow webserver -D
```
# run the Scheduler:
```
airflow scheduler -D
```

# check process is running
```
lsof -i tcp:8080

kill -9 <pid>
```

![output](https://github.com/MSaadMakhdoom/LSTM-model-training-pipeline-using-Apache-Airflow/blob/main/screencapture-localhost-8080-tree-2023-06-14-22_00_57.png)
##
![output](https://github.com/MSaadMakhdoom/LSTM-model-training-pipeline-using-Apache-Airflow/blob/main/screencapture-localhost-8080-graph-2023-06-14-22_01_16.png)

## DAG Script Code
![output](https://github.com/MSaadMakhdoom/LSTM-model-training-pipeline-using-Apache-Airflow/blob/main/screencapture-localhost-8080-code-2023-06-14-22_28_17.png)

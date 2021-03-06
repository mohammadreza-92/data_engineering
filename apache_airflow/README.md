This directory relates to some important notes about `Airflow`. 

In terms of data workflows, the following terms:
1. Automation training, testing, and deploying a machine learning model
2. Ingesting data from different REST APIs
3. Coordinating ETL, and ELT Processes Across an Enterprise Data Lake[1]


Basic Explanation: 

There are two types of executor - those that run tasks locally (inside the scheduler process), and those that run their tasks remotely (usually via a pool of workers). Airflow comes configured with the SequentialExecutor by default, which is a local executor, and the safest option for execution, but we strongly recommend you change this to LocalExecutor for small, single-machine installations, or one of the remote executors for a multi-machine/cloud installation.[2]

- `SequentialExecutor` is not recommended for a production setup, but it should not be an issue for our case.



References: 
1. [Medium Link](https://medium.com/abn-amro-developer/data-pipeline-orchestration-on-steroids-apache-airflow-tutorial-part-1-87361905db6d)
2. [Airflow](https://airflow.apache.org/docs/apache-airflow/stable/executor/index.html)

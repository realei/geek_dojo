 # AWS Airflow Common Knowledges 

## [Configuring the Amazon MWAA environment class](https://docs.aws.amazon.com/mwaa/latest/userguide/environment-class.html)

1. MWAA Infra Information: 

* A Celery Executor: AWS-managed AWS Fargate containers

* Airflow DB: AWS-managed Amazon Aurora PostgreSQL metadata database *where the Apache Airflow schedulers creates task instances*

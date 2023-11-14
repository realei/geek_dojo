# [Airflow Best Practices](https://airflow.apache.org/docs/apache-airflow/stable/best-practices.html#)

## System Design Improvement of Airflow

### Consistency:

1. Do not use INSERT during a task re-run, an INSERT statement might lead to duplicate rows in your database. Replace it with UPSERT.

2. Read and write in a specific partition. Never read the latest available data in a task. Someone may update the input data between re-runs, which results in different outputs. A better way is to read the input data from a specific partition. You can use `data_interval_start` as a partition. You should follow this partitioning method while writing data in `S3/HDFS` as well.

3. The Python datetime `now()` function gives the current datetime object. This function should never be used inside a task, especially to do the critical computation, as it leads to different outcomes on each run. It’s fine to use it, for example, to generate a temporary log.

4. Airflow executes tasks of a DAG on different servers in case you are using `Kubernetes executor` or `Celery executor`. Therefore, **you should not** store any file or config in the local filesystem as the next task is likely to run on a different server without access to it — for example, a task that downloads the data file that the next task processes. In the case of `Local executor`, storing a file on disk can make retries harder e.g., your task requires a config file that is deleted by another task in DAG.

Q1: accourding to 4th item, where to story `file` and `config`?

* XCom

* S3/HDFS

### Performance and Scalability of Airflow:

1. You should avoid writing the top level code which is not necessary to create Operators and build DAG relations between them.

2. performance

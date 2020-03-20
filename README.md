
```bash
export SPARK_HOME=$(pwd)/venv/lib/python3.7/site-packages/pyspark
export PYSPARK_DRIVER_PYTHON=jupyter
export PYSPARK_DRIVER_PYTHON_OPTS=notebook

pyspark --packages="org.apache.hadoop:hadoop-aws:2.7.3" --conf spark.hadoop.fs.s3a.aws.credentials.provider=com.amazonaws.auth.AnonymousAWSCredentials \
  --driver-java-options "-Dlog4j.configuration=file:/path/to/log4j-driver.properties -Dvm.logging.level=DEBUG"
```


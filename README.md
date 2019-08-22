# PySpark using Snowflake and OKTA 

## Init Setup
### Project bootstrapping

Initialize a new project in the current folder
```
# Setup a new venv to keep it clean
python3 -m venv venv

# Activate the virtual env
source venv/bin/activate

# Install all required packages in the virtual env
pip install -r requirements.txt 

# Install the new kernel with Jupyter
ipython kernel install --user --name=spark_snowflake

# Setup the env for pyspark (installed from pip)
export SPARK_HOME=`pwd`/venv/lib/python3.7/site-packages/pyspark
export PYSPARK_PYTHON=python3
export PYSPARK_DRIVER_PYTHON=jupyter
export PYSPARK_DRIVER_PYTHON_OPTS=notebook

# Run Jupyter and Spark
pyspark --packages net.snowflake:snowflake-jdbc:3.8.7,net.snowflake:spark-snowflake_2.11:2.5.1-spark_2.4
```

Update deps if needed later on:
```
pip freeze > requirements.txt
```


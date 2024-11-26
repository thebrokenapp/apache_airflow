# Installation

### Create virtualenv
```bash
python3 -m venv /path/to/virtualenv/directory
source bin/acticate
```

### Install Airflow
```bash
pip install apache-airflow
```

### Initialize the metastore (a database in which all Airflow state is stored)
```bash
 airflow db init
```

### Create a user
```bash
airflow users create --username ankit --password ankit --firstname Ankit --lastname Sahay --role Admin --email ankit@thebrokenapp.in
```

### Copy the sample DAG into the DAGs directory
```bash
mkdir -p /home/ankit/airflow/dags/
cp download_rocket_launches.py ~/airflow/dags/
```

### Start Webserver
```bash
airflow webserver
```

### Start scheduler
```bash
airflow scheduler
```

## Optional Steps
### To create additional users
```bash
airflow users create \
--username admin \
--password admin \
--firstname Admin \
--lastname User \
--role Admin \
--email admin@example.com
```

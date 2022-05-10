cd airflow_stt
mkdir ./dags ./logs ./plugins
echo -e "AIRFLOW_UID=$(id -u)\nAIRFLOW_GID=0" > .env
docker-compose build
docker-compose up airflow-init
docker-compose up

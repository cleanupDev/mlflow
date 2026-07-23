ARG MLFLOW_VERSION=v3.14.0

FROM ghcr.io/mlflow/mlflow:${MLFLOW_VERSION}

RUN python -m pip install --no-cache-dir \
        "mlflow[auth]==3.14.0" \
        psycopg2-binary \
        boto3 \
    && python -c "import psycopg2, boto3, flask_wtf; import mlflow.server.auth"

EXPOSE 5000

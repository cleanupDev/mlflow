ARG MLFLOW_VERSION=v3.14.0

FROM ghcr.io/mlflow/mlflow:${MLFLOW_VERSION}

RUN MLFLOW_PY_VERSION="$(python -c 'from importlib.metadata import version; print(version(\"mlflow\"))')" \
    && python -m pip install --no-cache-dir \
        "mlflow[auth]==${MLFLOW_PY_VERSION}" \
        psycopg2-binary \
        boto3 \
    && python -c "import psycopg2, boto3, flask_wtf, bcrypt"

EXPOSE 5000

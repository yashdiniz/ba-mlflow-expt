## MLFlow tracking APIs

# activate mlflow
mlflow server --backend-store-uri sqlite:///./MLFlow/store.db --default-artifact-root ./MLFlow/MLartifacts -h 127.0.0.1 -p 5000


## MLFlow model serve

# activate mlflow
set MLFLOW_TRACKING_URI=http://127.0.0.1:5000
mlflow models serve --no-conda -m "models:/dev.cb-wine-quality.ml@challenger" -p 8080

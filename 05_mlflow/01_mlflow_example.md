## 1. Start MLflow
```
cd 02_mlops_docker

docker-compose up --build -d mlflow mysql minio

cd ~
```

## 2. Move notes to vm

- Open browser:  http://127.0.0.1:500

## 3. Start Jupyter Lab
- Activate ds-dev 

` conda activate ds-dev ` 

- Start jupyter lab  

` jupyter lab --ip 0.0.0.0 --port 8990  `  

- Copy link and paste to browser

- Create a ds-dev notebook

- Import **mlflow-example.ipynb**

- Run notebook

- Open mlflow web ui and see the experiment and artifact.



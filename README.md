# MLFLOW
### Command used to launch the MLFlow server:
####      In the terminal enter the following command:
      mlflow server --backend-store-uri mlruns/ --default-artifact-root mlruns/ --host 0.0.0.0 --port 5000
#### to deploy
 mlflow models serve -m  ./mlruns/748421089920690936/a32358ed0e2a4553b296a9c4d5098323/artifacts/model -
p 8001 --no-conda
#### type the curl command in the another terminal simultaneoulsy
curl -X POST -H "Content-Type: application/json" --data '{"instances": [[12.8, 0.029, 0.48, 0.98, 6.2, 29, 3.33, 1.2, 0.39, 75, 0.66]]}' http://0.0.0.0:8001/invocations
<br>we get the prediction value here
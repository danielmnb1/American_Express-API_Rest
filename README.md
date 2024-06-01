docker build -t american . --> crear la imagen

docker run -p 3000:3000 -it --name american american --> hacer un docker con la iamgen creada y ver el cmd del docker en tiempo real

docker exec -it 21cd96a1dea74 /bin/bash --> entrar a los archivos del docker

docker ps ---> ver docker creados

docker images --> ver imagenes creadas


docker cp nombre_contenedor:ruta_del_archivo_dentro_del_contenedor directorio_destino_en_mi_computadora
docker cp american:/app/data/prediction_file.csv "C:\Users\Cristian\Downloads\modelos\American Express-Entrenamiento-prediccion-Api"

python .\predict.py --input_file=data/test_data.csv --predictions_file=data/prediction_file.csv --model_file=modelo_final.pkl   

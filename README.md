#crear y dockerizar fastapi

#crear archivo main.py
# main.py

from fastapi import FastAPI

app = FastAPI()

@app.get("/")
def read_root():
    return {"message": "Hello, World!"},

#crear Dockerfile
#crear el archivo requirements.txt
#construir la imagen docker
docker build -t <nombre-imagen> .

#verificar imagenes 
docker images
#ejecutar el contenedor
docker run -d -p 80:80 --name  fastapi-app

#verificar que la imagen se haya creado correctamente
docker build -t <nombre-imagen> .

#ejecucion de la imagen docker
docker run -d --name <nombre-contenedor> <nombre-imagen>

#verificar que este corriendo
docker ps

#detener la imagen
docker stop <nombre-contenedor>

#eliminar la imagen
docker rm <nombre-contenedor>


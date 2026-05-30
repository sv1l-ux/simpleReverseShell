# simpleReverseShell
Laboratorio para tener una reverse shell de forma simple.

## Paso 1: Descarga el archivo lab-app y descomprime.

## Paso 2: Ejecuta los siguientes comandos para instalar docker y plugins
`sudo apt update`

`sudo apt install docker.io docker-compose-plugin -y`

## Paso 3: Asegúrate de esta en el directorio en el que descomprimiste lo descargado y despliega la app
`sudo docker build -t vulnerable-app .`
`sudo docker run -d --name vulnerable-app -p 5000:5000 vulnerable-app`

> Nota: Para asegurarte que esté runeando la app, puedes usar el comando: `sudo docker ps` y debe salir algo como STATUS UP x seconds.

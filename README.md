
# Intruciones para probar puertos y conectividad para el cluster.

A continuación encontrarás varias instrucciones para ejecutar comandos para probar la conectividad de cada herramienta.

## Github
Basta con hacer **clone** al repositorio del bootcamp:
```
git clone https://github.com/ibm-cloud-academy/LightBlueCompute
```
## IBM Cloud cli
Una vez instalado el IBM Cloud CLI, asegúrate que se haya instalado correctamente al correr el comando:
```
ibmcloud 
```
Deberá mostrar las diferentes opciones de comandos que se puedan ralizar con esa herramienta.
La respuesta esperada sería algo así:
```
NOMBRE:
  ibmcloud - Una herramienta de línea de mandatos para interactuar con IBM Cloud
Encontrará más información en: https://ibm.biz/cli-docs

USO:
  [environment variables] ibmcloud [global options] command [arguments...] [command options]

VERSIÓN:
  1.6.0+59b6322-2021-05-26T20:35:50+00:00

MANDATOS:
  api                                   Establecer o ver el punto final de la API de destino
  login                                 Conectar usuario
  target                                Defina o visualice la región, la cuenta, el grupo de recursos, la organización o el espacio de destino
  config                                Escribir valores predeterminados para la configuración
  update                                Actualizar CLI a la versión más reciente
  [...]
```
Por último ejecuta el comando:
```
 ibmcloud login -r 'us-south'
```
Este útlimo camando debería mostrarte el resumen de la configuración de la herramienta CLI:
```
Punto final de API:         https://cloud.ibm.com   
Región:                     us-south   
Usuario:                    <micorreo@dominio.com>
Cuenta:                     <micuenta>   
Grupo de recursos:          default   
Punto final de API de CF:      
Organización:                  
Espacio:            
```
## Docker

Primero hay que iniciar Docker. Una vez inicio correr el siguiente commando:
```
 docker run hello-world
```
Se espera el siguiente resultado:

```
Unable to find image 'hello-world:latest' locally
latest: Pulling from library/hello-world
b8dfde127a29: Pull complete
Digest: sha256:9f6ad537c5132bcce57f7a0a20e317228d382c3cd61edae14650eec68b2b345c
Status: Downloaded newer image for hello-world:latest

Hello from Docker!
This message shows that your installation appears to be working correctly.

To generate this message, Docker took the following steps:
 1. The Docker client contacted the Docker daemon.
 2. The Docker daemon pulled the "hello-world" image from the Docker Hub.
    (amd64)
 3. The Docker daemon created a new container from that image which runs the
    executable that produces the output you are currently reading.
 4. The Docker daemon streamed that output to the Docker client, which sent it
    to your terminal.

To try something more ambitious, you can run an Ubuntu container with:
 $ docker run -it ubuntu bash

Share images, automate workflows, and more with a free Docker ID:
 https://hub.docker.com/

For more examples and ideas, visit:
 https://docs.docker.com/get-started/
```

### *Opcionalmente*
se recomienda crear una cuenta en hub.docker.com y una vez creada la cuenta se puede realizar 
el siguiente comando para autenticarse.
```
docker login 
```
## Mybluemix.net
Para probar la conexión a mybluemix.net se recomienda realizar una petición desde el browser a esta [dirección](https://bootcamp-gradle-build.mybluemix.net/ms/customer).

Así mismo desde la terminal se recomienda ejecutar el siguente comando. Simplmente descargará un jar de una de las aplicaciones que utilizaremos 
desde los laboratorios. 
```
curl https://bootcamp-gradle-build.mybluemix.net/ms/customer --output app.jar
```
## NodeJS
Una vez instalado NodeJS. Crearemos un proyecto sencillo de NodeJS e instalaremos la dependencia
de ExpressJS simplemente para poder validar que tenemos conectividad a través de NPM. 
Crear un directorio para realizar la prueba. Despues correr un comando de 
```
npm install init
```
Dar enter para dejar todo en default.
El resultado sería algo así:
```
This utility will walk you through creating a package.json file.
It only covers the most common items, and tries to guess sensible defaults.

See `npm help init` for definitive documentation on these fields
and exactly what they do.

Use `npm install <pkg>` afterwards to install a package and
save it as a dependency in the package.json file.

Press ^C at any time to quit.
package name: (tmp)
version: (1.0.0)
description:
entry point: (index.js)
test command:
git repository:
keywords:
author:
license: (ISC)
About to write to /Users/josef/dev/tmp/package.json:

{
  "name": "tmp",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "author": "",
  "license": "ISC"
}


Is this OK? (yes)
```

Ahora por favor correr el comando de:
```
npm install --save express
```
Y su resultado sería así:
```
added 50 packages, and audited 51 packages in 1s

found 0 vulnerabilities
```






# Vehicle Map

Procesamiento y visualización de coordenadas de vehículos en un mapa.

Unificación de repositorios vehicle-map y vehicle-front que componen el proyecto completo e inclusión en contenedor Docker.

## Instalación

Clonar este repositorio con submódulos. Usar el comando
  
```
git clone --recurse-submodules https://github.com/DiePalma/vehicle-project.git
```
 > Si no se agrega --recurse-submodules, se descargará el proyecto
> con dos directorios vacíos que corresponden a los repositorios vehicle-map y vehicle-front

Si se desea, comprobar el estado de los repositorios descargados, visualizando el commit actual usando 
```
git submodule status
```

## Ejecución

Dentro del directorio vehicle-project, abrir un terminal **bash** (CMD o Powershell no funcionarán) y ejecutar el comando 

```
docker-compose up
```

Esto inicializará los servidores de backend y frontend. Desde un navegador se puede entrar a ```localhost``` para acceder al frontend.
Para alimentar la base de datos, se puede realizar una solicitud post a ```localhost:3000/api/v1/gps``` con los datos de las coordenadas, identificador del vehículo y datos de hora y fecha.

## Entrega 3 Fernando Martinez

El objetivo de este entregable es que el script de la segunda entrega corra en un conteiner de Docke y
esté embebido en un DAG de Airflow dentro del container.

1) Como primer paso obtenemos la siguiente imagen de Docker Hub a nuestra máquina local (https://hub.docker.com/r/puckel/docker-airflow) mediante el comando **docker pull puckel/docker-airflow** 

2) Creo la carpeta DAG dentro del disco C:. Allí guardo el script de la segunda entrega con el nombre covid_data_dag.py

![image](https://github.com/fero1987/Curso-DE-CoderHouse/assets/50931047/a1e31afa-3d76-4de0-9e87-e3e1b032df78)

3) Creo el Dockerfile con el siguiente script

![image](https://github.com/fero1987/Curso-DE-CoderHouse/assets/50931047/0a64e789-2cc6-4093-9413-4e9961fb3604)

4) Creo el container con el comando **docker build -t imagen1 .**

![image](https://github.com/fero1987/Curso-DE-CoderHouse/assets/50931047/d850f007-12e6-406d-a650-96a444288e42)

5) Corro el container con el comando **docker run -d -p 8080:8080 imagen1**

![image](https://github.com/fero1987/Curso-DE-CoderHouse/assets/50931047/c7a1c8b8-1eb1-457d-9b44-c7e6a1817585)

6) Entro al puerto 8080, accedo a Airflow y ejecuto el DAG
   
![image](https://github.com/fero1987/Curso-DE-CoderHouse/assets/50931047/39446052-4d3e-4b1a-8612-b2e3485fa90b)

7) En la vista de (Tree View) vemos como viene la ejecución del DAG

![image](https://github.com/fero1987/Curso-DE-CoderHouse/assets/50931047/f5883190-25a8-40e2-a45d-f94c188aa99b)

8) Accedo al log para ver la correcta ejecución del script. Aquí podemos observar como se fueron ejecutando todos los pasos del script covid_data_dag.py

![image](https://github.com/fero1987/Curso-DE-CoderHouse/assets/50931047/fea02092-6b16-4abf-a776-c5740b49318e)
![image](https://github.com/fero1987/Curso-DE-CoderHouse/assets/50931047/fdfe12e0-5ade-4b4a-80f5-e23fc5b742ca)


   
10) 

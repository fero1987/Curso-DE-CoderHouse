## Entregable 3 Fernando Martinez

El objetivo de este entregable es que el script de la segunda entrega corra en un conteiner de Docke y
esté embebido en un DAG de Airflow dentro del container.

1) Como primer paso obtenemos la siguiente imagen de Docker Hub a nuestra máquina local (https://hub.docker.com/r/puckel/docker-airflow) mediante el comando **docker pull puckel/docker-airflow** 

2) Creo la carpeta "dag" dentro del repositorio. Allí guardo el script de la segunda entrega con el nombre covid_data_dag.py. Las modificaciones que se le hicieron a este script fue para crear distintas tareas a ejecutarse en AIRFLOW.

3) Creo el Dockerfile con el siguiente script.

![image](https://github.com/fero1987/Curso-DE-CoderHouse/assets/50931047/0a64e789-2cc6-4093-9413-4e9961fb3604)

4) Creo el container con el comando **docker build -t imagen1 .**

![image](https://github.com/fero1987/Curso-DE-CoderHouse/assets/50931047/d3495506-1982-4f35-80e7-9f781823907b)

5) Corro el container con el comando **docker run -d -p 8080:8080 imagen1**

![image](https://github.com/fero1987/Curso-DE-CoderHouse/assets/50931047/7815c98c-399a-4615-a758-d5c6fb325dcd)

6) Entro al puerto 8080, accedo a Airflow y ejecuto el DAG.
   
![image](https://github.com/fero1987/Curso-DE-CoderHouse/assets/50931047/39446052-4d3e-4b1a-8612-b2e3485fa90b)

7) En la vista de (Tree View) vemos como viene la ejecución del DAG.

![image](https://github.com/fero1987/Curso-DE-CoderHouse/assets/50931047/124d9a20-e2ae-4ece-8bab-fa38f588c255)

8) Vemos que se han ejecutado todas las tareas con éxito.

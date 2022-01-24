
# Pipeline en Jenkins.

![Logo-pipeline-Jenkins](capturas/logo-pipeline-jenkins.jpg)

## 1. Introducción.

En esta guiá veremos que son la Pepeline en Jenkins y realizaremos la construcción de un Pipeline de los siguiente : maven,  node, rubi, python, php, go.

Las pipeline en Jenkins es un conjunto de procesos que sigue aplicaciones desde un repositorio como puede ser por ejemplo Git.

Digamos que la pipeline es la linea de procesos o pasos que realizamos para el testeo o despliegue de un programa o aplicación en concreto, por ejemplo los pasos para validar que nuestra aplicaciones pasa por todos los test.

Para definir las pipelines en Jenkins, se describe en un fichero de texto llamada Jenkinsfile que se puede subir al repositorio del proyecto, permitiéndonos revisar ciclo del codigo, crear automáticamente la pipe para todas las ramas y pull de proyecto… El Jenkinsfile se puede definir de dos maneras declarativa ó guionizada.


## 2. Preparación. 
Antes de ponernos a crear las pipelines de los lenguaje vamos a preparar la maquina para evitar posibles errores durante el proceso.
Primero de todos vas a necesitar tener instalado tanto Jenkins como Docker si nos los tienes, en otras guiás explicamos como tenerlos instalados y configurados.

Con esto realizado vamos a acceder a Jenkins y tras iniciar secion vamos a "Administrar jenkins" > "Administrar Plugins"

![09-error-docker01](capturas/09-error-docker01.PNG)


Ya a aquí dentro vamos buscar dos plugins e instalarlos para ello vamos a la pestaña de “todos los plugin” y buscamos “Docker Commons Plugins” y "Docker Pipeline".

![09-error-docker02](capturas/09-error-docker02.PNG)


Y por ultimo después de reinstalar Jenkins y comprobar que los tenemos instalado vamos a un terminal y vamos a añadir el usuario jenkins al grupo de docker para que tenga permisos.

``` 
sudo usermod -a -G docker jenkins
```

![09-error-docker03](capturas/09-error-docker03.PNG)

## 3. Crear pipeline.
Ahora vamos a proceder con la creación de las pipeline de los lenguaje, esto lo realizamos pulsando en "Nueva Tarea" > Pipeline.

![01-nueva-tarea](capturas/01-nueva-tarea.PNG)


**Maven**
Introducimos el nombre y el tipo Pipeline.

![02-maven-pipeline01](capturas/02-maven-pipeline01.PNG)

Vamos “Advanced Proyecto Options” y añadimos el script con la sintaxis de pipeline correcta.

![02-maven-pipeline02](capturas/02-maven-pipeline02.PNG)

Tras guardar pinchamos en "Construir ahora" y al terminar en la misma pagina veremos el stage de los pasos.

![02-maven-pipeline03](capturas/02-maven-pipeline03.PNG)

![02-maven-pipeline04](capturas/02-maven-pipeline04.PNG)

**Rubi**
Seguimos los mismos pasos ya descritos.

Introducir el nombre.

![03-rubi-pipeline01](capturas/03-rubi-pipeline01.PNG)

Crear el script.

![03-rubi-pipeline02](capturas/03-rubi-pipeline02.PNG)

Construcción y finalización.

![03-rubi-pipeline03](capturas/03-rubi-pipeline03.PNG)

![03-rubi-pipeline04](capturas/03-rubi-pipeline04.PNG)

**Node**
Introducir el nombre.

![04-node-pipeline01](capturas/04-node-pipeline01.PNG)

Crear script.

![04-node-pipeline02](capturas/04-node-pipeline02.PNG)

Construcción y finalización.

![04-node-pipeline03](capturas/04-node-pipeline03.PNG)

![04-node-pipeline04](capturas/04-node-pipeline04.PNG)


**Python**

Introducir nombre.

![05-python-pipeline01](capturas/05-python-pipeline01.PNG)

Crear script.

![05-python-pipeline02](capturas/05-python-pipeline02.PNG)

Construcción y finalización.

![05-python-pipeline03](capturas/05-python-pipeline03.PNG)

![05-python-pipeline04](capturas/05-python-pipeline04.PNG)

**PHP**

Introducir nombre.

![06-php-pipeline01](capturas/06-php-pipeline01.PNG)

Crear script.

![06-php-pipeline02](capturas/06-php-pipeline02.PNG)

Construcción y finalización.

![06-php-pipeline03](capturas/06-php-pipeline03.PNG)

![06-php-pipeline04](capturas/06-php-pipeline04.PNG)

**Go**

Introducir nombre.

![07-go-pipeline01](capturas/07-go-pipeline01.PNG)

Crear del script.

![07-go-pipeline02](capturas/07-go-pipeline02.PNG)

Construcción y finalización.

![07-go-pipeline03](capturas/07-go-pipeline03.PNG)

![07-go-pipeline04](capturas/07-go-pipeline04.PNG)


Al ir realizando veremos como en el panel de control nos iran apareciendo todas las pipelines que hemos creado, si se han realizado correcctamente veremos un ok.

![08-tareas-realizadas](capturas/08-tareas-realizadas.PNG)
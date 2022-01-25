
# Creación de Pipeline en PHP y Apache

![logo-pipeline-jenkins](capturas/logo-pipeline-jenkins.png)


## 1. Introducción.
En esta guiá vamos a contruir una pipeline de un proyecto en Github.

## 2. Preparación. 
Primero de todo debemos crear el proyecto que vamos a subir a github, por lo que vamos a crear un nuevo repositorio en nuestro github. En este caso lo hemos nombrado "php-helloworld".


![01-new-proyect](capturas/01-new-proyect.png)




Nos lo clonamos en nuestra maquina para empezar a trabajar.


![02-clone](capturas/02-clone.png)


Y creamos una estructura básica que estará formada por una carperta src donde se encuentra un fichero "index.php" y una carpeta con un imagen que se va a mostrar en la página.


![03-estrucutra](capturas/03-estrucutra.png)


Contenido del fichero "index.php".

![04-index](capturas/04-index.png)


Ahora vamos a crear un fichero Dockerfile para crear un contenedor apache-php que nos permite desplegar nuestra pagina. También vamos a crear un fichero Jenkinsfile con los pasos que hay realizar en la pipeline. Todos estos fichero irán en la raíz del repositorio.

Fichero Dockerfile.


![05-docker](capturas/05-docker.png)


Fichero Jenkinsfile

![06-jenkinsfile](capturas/06-jenkinsfile.png)


Con esto realizado vamos a realizar un push de nuestro repositorio para subirlo a Github.


![07-push](capturas/07-push.png)


## 3. Creación Pipeline.
Con los pasos anteriores realizado vamos a nuestro Jenkins y creamos un nueva pipeline.

Creamos el nuevo pipeline.

![08-create-pipeline](capturas/08-create-pipeline.png)


Nos vamos al apartador de "Advanced Proyect Options" añadimos la configuración siguiente.

![09-añadir-repositorio.png](capturas/09-añadir-repositorio.png)


Pipeline creada.

![10-creada-pipeline](capturas/10-creada-pipeline.png)


Pulsamos en "Construir ahora" para lanzar el pipeline.

![11-lanzar-pipeline.png](capturas/11-lanzar-pipeline.png)


Si toda ha ido bien veremos algo como lo siguiente.
![12-pipeline-terminado](capturas/12-pipeline-terminado.png)



Y en el panel de control veremos lo siguiente.

![13-pipeline-soleado](capturas/13-pipeline-soleado.png)


No habría necesidad de probar la pagina ya que el step de "probar página" de pipeline esta ok, pero si accedes al puerto por un navegador podremos ver la página.

![14-pagina](capturas/14-pagina.png)
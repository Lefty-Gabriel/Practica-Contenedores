# TAS1 - Estructura

## 1. Título

**Creación y personalización de dos servidores web con Nginx usando Docker**

## 2. Tiempo de duración

2 horas 

## 3. Fundamentos

### Docker

Docker es una plataforma de virtualización basada en contenedores que permite crear, ejecutar y administrar aplicaciones en entornos aislados. Los contenedores comparten el núcleo del sistema operativo anfitrión

En esta práctica, utilicé Docker para crear dos contenedores independientes, cada uno con su propia configuración de publicación de puertos y contenido web.

### Contenedores e imágenes Docker

Una imagen Docker es una plantilla que contiene los elementos necesarios para ejecutar una aplicación o cualquier proyecto que estemos desarrollando.
En la práctica se utilizó la imagen oficial de Nginx para crear dos contenedores denominados `nginx1` y `nginx2`. Aunque ambos se basan en la misma imagen, funcionan de manera independiente y pueden presentar contenidos web diferentes.

<img width="1232" height="451" alt="Captura de pantalla 2026-10-15 215959" src="https://github.com/user-attachments/assets/f375b2fc-bf6e-4357-8342-9cda7d474dc4" /> Nota: Esta es la interfaz grafica de docker

### Servidor web Nginx

Nginx es un servidor web de código abierto que permite atender solicitudes HTTP y entregar contenido estático, como archivos HTML, hojas de estilo CSS, imágenes y otros recursos web.

<img width="738" height="306" alt="images" src="https://github.com/user-attachments/assets/da168044-7bae-4250-89f7-0b15a693811a" />


## 4. Conocimientos previos

- Conceptos básicos de virtualización y contenedores.
- Instalación y uso básico de Docker.
- Manejo de comandos en PowerShell o una terminal de comandos.
- Conocimientos básicos de HTML para editar y personalizar páginas web.
- Comprensión del funcionamiento de un servidor web y del protocolo HTTP.
- Conocimiento básico de puertos de red y direcciones locales.
- Manejo de archivos y directorios en el sistema operativo anfitrión.


## 5. Objetivos a alcanzar

- Crear dos contenedores independientes a partir de la imagen oficial de Nginx.
- Configurar la publicación de puertos para acceder a cada servidor desde el navegador.
- Utilizar el comando `docker cp` para transferir archivos entre los contenedores y el sistema anfitrión.
- Modificar el archivo `index.html` para incorporar información relacionada con el instituto.
- Comprobar el funcionamiento de ambos servidores mediante el acceso a sus direcciones locales.

## 6. Equipo necesario

-Laptop
-Terminal powershell
-Docker

## 7. Material de apoyo

- Documentación oficial de Docker.
- Documentación oficial de Nginx.
- Terminal PowerShell para ejecutar los comandos.
- Imagen oficial de Nginx disponible en Docker Hub.
- Editor de texto para modificar el archivo HTML.
- Capturas de pantalla de los comandos ejecutados y de las páginas web obtenidas.

## 8. Procedimiento

Paso 1: se hizo un pull de la imagen de nginx para poder trabajar, luego se creo el contenedor configurando sus puertos a exponer 

<img width="1600" height="618" alt="Captura de pantalla 2026-10-15 145848" src="https://github.com/user-attachments/assets/2fa96fe8-6ae3-4099-af59-95fffabd7beb" />


Paso 2: Luego se copio el archivo de index.html hacia la laptop para poder trabajar con esta

<img width="1321" height="85" alt="Captura de pantalla 2026-10-15 150050" src="https://github.com/user-attachments/assets/9d9f2c3b-8084-46e7-9c91-d55ddc776828" />


Paso 3: se edito el archivo index.html con el editor de texto nano 

<img width="1475" height="700" alt="Captura de pantalla 2026-10-15 160312" src="https://github.com/user-attachments/assets/753d4f33-67db-42a4-be28-4f7354193ac8" />


Paso 4: se creo el segundo contenedor y se hizo uso del comando cp para copiar este archivo ya editado hacia la ruta donde se encontraba mi contenedor de docker 

<img width="1383" height="172" alt="Captura de pantalla 2026-10-15 160750" src="https://github.com/user-attachments/assets/ad1edaf4-ac4a-4016-87e6-ac7caed920e7" />


Paso 5: con el primer contenedor ya creado se volvio a editar el mismo archivo html ya que el primer contenedor ya guardo su estado 

<img width="1467" height="612" alt="Captura de pantalla 2026-10-15 160805" src="https://github.com/user-attachments/assets/8a5dc87f-d1ad-414c-af0d-5fb3fd8a4853" />


Paso 6: se copio este archivo ya editado al otro contenedor 

<img width="1283" height="150" alt="Captura de pantalla 2026-10-15 222012" src="https://github.com/user-attachments/assets/1c25eeab-717c-4a65-be71-c46bd26f76f3" />


Paso 7: verificar el estado de estos contenedores 

<img width="1917" height="1015" alt="Captura de pantalla 2026-10-15 160347" src="https://github.com/user-attachments/assets/6f73d7a6-d0c0-4761-ab0f-d2a6f6685ba7" />

<img width="1917" height="1015" alt="Captura de pantalla 2026-10-15 161019" src="https://github.com/user-attachments/assets/208a4fa0-e801-4297-b519-481c4bc9c42d" />


## 9. Resultados esperados

- Dos contenedores Docker creados a partir de la imagen oficial de Nginx.
- Un primer servidor web accesible mediante `http://localhost:8089`.
- Un segundo servidor web accesible mediante `http://localhost:8090`.
- Una página HTML personalizada en el contenedor `nginx1` con información relacionada con el instituto.
- Una transferencia de archivos realizada correctamente entre el sistema anfitrión y el contenedor mediante `docker cp`.
- Una comprobación satisfactoria del acceso a los dos servidores desde el navegador.
  
## 10. Bibliografía

Docker, Inc. (s. f.). *docker container cp*. Docker Docs. https://docs.docker.com/reference/cli/docker/container/cp/

Docker, Inc. (s. f.). *Official Nginx image*. Docker Hub. https://hub.docker.com/_/nginx

F5, Inc. (s. f.). *NGINX documentation*. https://nginx.org/en/docs/


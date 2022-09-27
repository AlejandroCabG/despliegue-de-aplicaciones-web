## Ejercicio 1
Repositorio creado en GitHub => https://github.com/AlejandroCabG/despliegue-de-aplicaciones-web.git

## Ejercicio 2
Véase imágen Ex_02.PNG.

## Ejercicio 3
La estructura de solicitud está formada por un *_método_*, que indica que tipo de solicitud es (pueden ser GET, POST O HEAD); la *_ruta_* que forma parte de la url que viene después del dominio /moodel/course/view.php?id=29 HTTP/1.1 y finalmente el protocolo, que en este caso es HTTP 1.1.
El resto de datos que se envían son el host, la lengua y el encode (gzip) junto con el anvegador empleado.
Véase imágenes Ex_03.PNG y Ex_031.PNG

## Ejercicio 4 
El puerto al que se reciben normalmente las peticiones del protocolo HTTP es el 80/TCP, que es el puerto por defecto.
El protocolo HTTP se encuentra en la capa 4 o capa de aplicación, ya que en esta se encuentran los protocolos que proporcionan servicios de usuario o intercambio de datos de aplicaciones de las connexiones de red establecidas por los protocolos de red de capas inferiores. 
El protocolo TCP pertenece a la capa 1 o capa de acceso al medio, que es la capa más baja y también a la capa 3 o capa de transporte, que es la capa donde se establecen canales de datos básicos utilizadas para hacer posoble el intercambio de datos.
El protocolo UDP, protocolo de datagramas no orientado a conexión, pertenece a la capa 3 como TCP pero no es muy fiable a ligual que el IP, y se emplea para aplicaciones de transmisión de medios (audio, vídeo, voz sobre IP). 
El protocolo IP pertenece a la capa 1 y a la capa 2 o capa de internet, que consta de dos sistemas de direccionamiento para identificar lso hosts de la red y ubucarlos en la red. Estos son el Protocolo de internet versión 4 (IPv4) para direcciones de 32 bits y el Protocolo de internet versión 6 (IPv6) para direcciones de 128 bits. 

## Ejercicio 5
*HTTP/1.1 302 Found* es el código de estado de redirección HTTP, que indica que el recurso solicitado ha sido movido temporalmente a la URL dada por las cabeceras Location (en-US). El navegador redirecciona a la página, pero los motores de búsqueda no actuaizan los enlaces al recurso.

## Ejercicio 6
Lo primero es abrir el navegador y acceder a www.google.com. Después ejecutamos el programa y pulsando sobre la red (en mi caso WI-FI) ejecutamos la "captura de paquetes". Una vez empiece el programa captura todos los paquetes especificando el número, tiempo, dirección, destinatario y protocolo. 
Del número 15 al 18 se puede observar la comunicación con la aplicación (Aplication Data) y el desglose en paquetes mediante TCP, así como mi dirección IP (192.168.145) y la IP (142.250.184.10) que es la del host de google. Si introduzco la IP 142.250.184.10, accedo a Google.
Véase imágen Ex_06.PNG

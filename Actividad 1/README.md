## Ejercicio 1
**1. Crea un repositorio para subir todas las actividades de esta asignatura con el
nombre despliegue-de-aplicaciones-web.**
Repositorio creado en GitHub => https://github.com/AlejandroCabG/despliegue-de-aplicaciones-web.git

## Ejercicio 2
**2. Crea una carpeta en tu repositorio llamada “Actividad 1” y dentro crea un archivo
README.md con la solución a los siguientes ejercicios.**
En el perfil de GitHub he dado nombre a una carpeta llamada _Actividad_ 1 seguida de una **/** para añadir a su vez un archivo 
README.md.
Véase imágen Ex_02.PNG.

## Ejercicio 3
**3. Analiza los headers de las peticiones cuando inicias sesión en el Moodle y comprende
cómo se obtiene el token. Para ello, necesitamos saber de dónde salen TODOS los
datos sensibles que se envían.**
La estructura de solicitud está formada por un *_método_*, que indica que tipo de solicitud es (pueden ser GET, POST O HEAD); la *_ruta_* que forma parte de la url que viene después del dominio /moodel/course/view.php?id=29 HTTP/1.1 y finalmente el protocolo, que en este caso es HTTP 1.1.
El resto de datos que se envían son el host, la lengua, la codificación, la fecha, el servidor, el encode (gzip), las cookies, la referencia y junto con el navegador empleado.
El cliente envía los datos de login a través de un formulario. Si el login es correcto se autentifica y devuelve el token. Para acceder a posteriores accesos, se envía el token otra vez. El token se almacena en el lado de cliente para poder usarlo más tarde. El token tiene un tiempo de validez, que se establece en el servidor, que será rechazado i el cliente no podrá acceder a la información.
También se puede proporcionar un token de refresco para aumentar el tiempo de validez o generar uno nuevo, sin necesidad de obligar al usuario a volver a enviar su datos de inicio.
Para poder obtener el token se hace mediante una API REST el estado lo mantiene el cliente y por lo tanto es el cliente quien debe pasar el estado en cada llamada.
Véase imágenes Ex_03.PNG, Ex_031.PNG y Ex_032.PNG.

## Ejercicio 4 
**4. ¿A qué puerto se reciben normalmente las peticiones del protocolo HTTP? ¿A qué
capa del modelo TCP/IP se encuentra el protocolo HTTP? ¿Y los protocolos TCP,
UDP, e IP?**
El puerto al que se reciben normalmente las peticiones del protocolo HTTP es el 80/TCP, que es el puerto por defecto.
El protocolo HTTP se encuentra en la capa 4 o capa de aplicación, ya que en esta se encuentran los protocolos que proporcionan servicios de usuario o intercambio de datos de aplicaciones de las connexiones de red establecidas por los protocolos de red de capas inferiores. 
El protocolo TCP pertenece a la capa 1 o capa de acceso al medio, que es la capa más baja y también a la capa 3 o capa de transporte, que es la capa donde se establecen canales de datos básicos utilizadas para hacer posoble el intercambio de datos.
El protocolo UDP, protocolo de datagramas no orientado a conexión, pertenece a la capa 3 como TCP pero no es muy fiable a ligual que el IP, y se emplea para aplicaciones de transmisión de medios (audio, vídeo, voz sobre IP). 
El protocolo IP pertenece a la capa 1 y a la capa 2 o capa de internet, que consta de dos sistemas de direccionamiento para identificar lso hosts de la red y ubucarlos en la red. Estos son el Protocolo de internet versión 4 (IPv4) para direcciones de 32 bits y el Protocolo de internet versión 6 (IPv6) para direcciones de 128 bits. 

## Ejercicio 5
**5. ¿Cuál es el significado de la siguiente respuesta de un servidor?
HTTP/1.1 302 Found
Location: http://www.example.com/test/index2.php**
*HTTP/1.1 302 Found* es el código de estado de redirección HTTP, que indica que el recurso solicitado ha sido movido temporalmente a la URL dada por las cabeceras Location (en-US). El navegador redirecciona a la página, pero los motores de búsqueda no actuaizan los enlaces al recurso.

## Ejercicio 6
**6. Utilizando el filtro de captura para la interfaz de red de Wireshark, analiza la petición
al host: www.google.com. Mostrando la cabecera IP, la dirección IP de tu ordenador y
la del servidor. Comprueba que, poniendo esa IP en el navegador, accedas a Google.**
Lo primero es abrir el navegador y acceder a www.google.com. Después ejecutamos el programa y pulsando sobre la red (en mi caso WI-FI) ejecutamos la "captura de paquetes". Una vez empiece el programa captura todos los paquetes especificando el número, tiempo, dirección, destinatario y protocolo. 
Del número 15 al 18 se puede observar la comunicación con la aplicación (Aplication Data) y el desglose en paquetes mediante TCP, así como mi dirección IP (192.168.145) y la IP (142.250.184.10) que es la del host de google. Si introduzco la IP 142.250.184.10, accedo a Google.
Véase imágen Ex_06.PNG

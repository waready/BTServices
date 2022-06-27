# Instrucciones de configuración 

Para usar BTServicesExposer lo primero que se tiene que hacer son algunas configuraciones en los 
siguientes archivos de configuración.

## Paso 1 – Configurar aplicación Node

Primero hay que configurar el archivo config.js que se encuentra en la ruta `\BTExposer\config\config.js.` 
En el mismo hay una sección btservices donde se podrá configura los 
servicios a ser utilizados. 

Los datos para ingresar son:
Los siguientes 5 parámetros se completan si se usa autenticación oauth2, de lo contario se pueden 
dejan como string vacío

* **Canal**:  Nombre del canal. Identifica el canal o aplicación que utiliza el servicio
* **Requerimiento**: Requerimiento de los servicios
* **Usuario**: Nombre de usuario. Identifica el usuario de ejecución del requerimiento. Este  usuario debe ser válido para el canal que se está ejecutando en BTS
*  **Userid**: Nombre de usuario de los servicios Bantotal
*  **Userpassword**: Contraseña encritada para la authentication de los servicios (AES Encryptor)
*  **Protocol**: Las opciones de protocolos son http y https
*  **HostName**: IP o DNS del servidor
* **Port**: Puerto donde están publicados los servicios 
* **BaseUrl**: Base de la url de los servicios publicados
* **SSLPublicCert**: Ubicación certificado público para cifrado de datos
* **SSLAutoSigned**: ¿Es el certificado autofirmado? true | false
* **User**: parámetros por si se tiene autenticación básica
* **Pass**: parámetros encriptado por si se tiene autenticación básica (AES Encryptor)
* **headers**: User-Agent
* **authenticate**: ejemplo ‘odwsbt_Authenticate_v1?Execute’ (no poner package ni aspx)
* **plataform**: Las opciones de plataforma son JAVA o .NET 
* **prefijo**: En caso de estar trabajando con servicios de V3R1, hay que agregarle en el 
parámetro prefijo la opción de `“ardwsbt_” en vez de “odwsbt_”`. 

``` json

btservices:{
    Canal:"BTDIGITAL",
    Requerimiento:1,
    Usuario: "INSTALADOR",
    Userid: "MINSTALADOR",
    Userpassword:"U2FsdGVkX1/9/hjoJ2QCNI1iN4VDJtu2aR+6byblALQ~",
    Protocol:"http",
    HostName:"monitoreo2019",
    Post:"6015",
    BaseUrl:"/arqgx16sql/servlet",
    SSLPublicCert:"",
    SSLAutoSigned:false,
    User:"bantotal",
    Pass:"U2FsdGVkX19JZoxBwIzDjg64HFJAKALZEGz/GW2pAzI-",
    header:{
        "User-Agent":"",
    },
    authenticate:"ardwsbt_Authenticate?Execute",
    plataform:"JAVA",
},
prefijo:"ardwsbt_", //odwsbt_ o ardwsbt_
```

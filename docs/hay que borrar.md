# Wireshark

En los análisis que hacemos a través de Wireshark, nos fijamos principalmente en dos cosas: los Endpoints (es decir, los servdiores contactados) y el protoclo HTTP, que sería HTTP sin cifrar. En este pequeño tutorial explicaremos cómo identificar las conexiones HTTP y cómo analizar los servidores contactados.


## Endpoints

### Configuración   

Para realizar el análisis de endpoints, primero tenemos que configurar Wireshark.

1. Registrarse en esta [página](https://www.maxmind.com/en/geolite2/signup?lang=en). Es necesario hacerlo para poder descargar las bases de datos que necesitamos. 
2. Descargar los siguientes archivos:
    - GeoLite ASN 2
    - GeoLite2 City 
    - GeoLite2 Country    
3. Crea un directorio. En este caso le llamaremos MaxMind. En la carpeta de descargas vamos a descomprimir los archivos con extensión .tar.gz que acabamos de bajar. Las carpetas al interior van a tener un nombre similar a :
    - GeoLite2-ASN_20220614
    - GeoLite2-Country_20220614
    - GeoLite2-City_20220614

4. Dentro de cada de estas carpetas hay un archivo con extensión .mmdb. Extraer estos archivos y copiarlos al directorio MaxMind. 
5. En Wireshark ir a *File* --> *Preferences* --> *Name Resolution* --> *MaxMind Database Directories* (Edit)
6. Con el signo de - seleccionar cada directorio que exista ahí y borrarlo. 
7. Con el botón de + agregar la ruta al directorio de MaxMind.
8. Reiniciar Wireshark

### Datos

1. Abrir el archivo .pcap que se quiere analizar
2. Ir a *Statistics* --> *Endpoints* --> *IPv4*. Esto nos dará la lista de los servidores contactados y datos sobre ellos: 
    - Address: dirección IP
    - Packets: número total de paquetes enviados y recibidos
    - Bytes: la cantidad de información enviada y recibida
    - Tx Packets: número de paquetes enviados desde esa IP
    - Tx Bytes: cantidad de datos enviados desde esa dirección IP
    - Rx Packets: número paquetes recibidos por esa dirección IP
    - Rx Bytes: cantidad de datos recibidos por esa IP
    - Country: país donde está localizada la dirección IP
    - City: ciudad donde está localizada la dirección IP
    - AS Number: Número de sistema autónomo [ASN](https://es.wikipedia.org/wiki/Sistema_aut%C3%B3nomo) 
    - AS Organization: Organización a la que pertenece esa dirección IP

    Para nuestros análisis, lo que más nos importa es la geolocalización de las direcciones IP, lo que nos dice a dónde están yendo nuestros datos y la organización a la que pertencen (Google, Facebook, Uninet, etc.). Es importante señalar que muchas veces pueden aparecer organizaciones como [Akamai](https://www.akamai.com/es). Esta empresa, si bien proporciona productos de seguridad en la nube, es conocida por ser un [CDN](https://es.wikipedia.org/wiki/Red_de_distribuci%C3%B3n_de_contenidos)  (Content Distribution Network). Esto es importante recalcarlo ya que las organizaciones involucradas en una aplicación no tienen siempre la misma función. Algunas almacenan nuestros datos, otras sólo son proveedoras de contenido, otras sirven para proporcionar seguridad, otras son [DNS](https://es.wikipedia.org/wiki/Sistema_de_nombres_de_dominio), etc. 

    ### Protocolos

    Al hacer el análisis de un archivo .pcap, otra cosa que nos interesa son los protocolos de comunicación. Esto nos interesa porque nos dice qué tipo de información es probable que se esté intercambiando entre las diferentes direcciones IP y su función. Pondremos aquí algunos de los protocolos más comunes:

    - [ARP](https://es.wikipedia.org/wiki/Protocolo_de_resoluci%C3%B3n_de_direcciones) - Este protocolo sirve para identificar a qué aparato (router, computadora, celular, etc.) corresponde una cierta dirección IP local. En general, si nos fijamos en este protocolo, aparecerán los diferentes dispositivos que tenemos en nuestra red local y las diferentes direcciones IP locales. Estas direcciones, para el análisis que nos interesa, son superfluas. 
    - DNS - Este protocolo sirve para convertir los nombres de las direcciones IP a formatos legibles por seres humanos. El uso más frecuente y famoso es el de traducir una dirección IP a un nombre de dominio como www.google.com
    - [HTTP](https://es.wikipedia.org/wiki/Protocolo_de_transferencia_de_hipertexto) - Este protocolo sirve para enviar datos entre diferentes direcciones IP. Es uno de los que nos interesa en términos de seguridad, ya que, al no estar cifrado, es muy suceptible a ser abusado, de tal manera que un actor malintencionado pueda acceder a información sensible y privada.
    - [HTTPS](https://es.wikipedia.org/wiki/Protocolo_seguro_de_transferencia_de_hipertexto) - Es igual al protocolo anterior, pero está cifrado, de tal manera que los datos que se comparten entre diferentes direcciones IP viajan más seguros ya que es mucho más difícil acceder a ellos.
    - OpenVPN - Este protocolo es el protocolo de comunicaciones de la Red Privada Virtual que estamos utilizando, OpenVPN. En general aquí se encontrará la dirección IP local y nuestra dirección IP pública. (Recuerda que si quieres hacer públicos los datos de tu análisis, es importante borrar tu dirección IP pública).
    - [TCP](https://es.wikipedia.org/wiki/Protocolo_de_control_de_transmisi%C3%B3n) - Protocolo que está al nivel de la acpa de transporte en el modelo [OSI](https://es.wikipedia.org/wiki/Modelo_OSI). Gracias a este, otros protocolos, como HTTP, pueden funcionar. 
    - [TLS] (https://es.wikipedia.org/wiki/Seguridad_de_la_capa_de_transporte) - Al igual que el TCP, se encuentra en la capa de transporte del modelo OSI. Es un protocolo criptográfico que permite establecer comunicaciones seguras. Probablemente aparezca en Wireshark como TLSv1.3, que hace referencia a la versión que se usa actualmente.
    - [UDP](https://es.wikipedia.org/wiki/Protocolo_de_datagramas_de_usuario) - Protocolo similar a TCP y que tiene la misma función. La diferencia radica en que TCP tienen integrado un método para revisar que los paquetes llegaron al lugar correcto y de forma correcta, mientras que UDP no. De esta manera, TCP es más fiable, pero más lento. Dependiendo del tipo de datos que se estén enviando uno u otro será más efectivo. 

    __Conclusiones__    
    De todos estos protocolos los que nos interesan son el HTTP y el HTTPS que es por donde viajan los datos que nos interesa analizar. 

    ### Direcciones [IP](https://es.wikipedia.org/wiki/Direcci%C3%B3n_IP)

    Dentro del análisis de los Endpoints, nos encontraremos a grandes rasgos tres tipos de direcciones IP. 
    - Direcciones del tipo: 192.168.x.x o 10.x.x.x Estas direcciones son llamadas IP privadas o IP locales. Son las direcciones que cada uno de nuestros aparatos tiene como identificador único. Para nuestro análisis no son importantes. 
    - Direcciones pertenecientes a DNS públicos. De los más famosos son los de Google: 8.8.8.8 y 8.8.4.4; Cloudflarenet 1.1.1.1 y 1.0.0.1 y AdGuard 94.140.14.14 y 94.140.15.15 Cuando se configura el cliente de OpenVPN en el servidor de Ubuntu, se puede escoger el DNS preferido. Tomar nota de esto, para identificar las direcciones IP que se hacen a ese servicio. Vale la pena mencionar que uno puede alterar el servidor DNS tanto del sistema operativo como del router mismo, y esto es algo que, en cuanto a privacidad, se menciona poco. 
    - Direcciones pertenecientes a las empresas. Estas pueden variar en su forma. 

    __Conclusiones__   
    Al realizar el análisis de las direcciones IP, es importante saber identificar, al menos, las IP locales y las que pertenecen al servidor DNS que tengamos configurado.  

## Mapas
Otra función de Wireshark es la posibilidad de visualizar la geolocalización de las diferentes direcciones IP en un mapa. 
- En la ventana de *Endpoints*, en la esquina inferior derecha, podemos seleccionar *Map* --> *Open in Browser*. En el mapa aparecerán los lugares y el número de conexiones que se establecieron con dicha dirección IP.

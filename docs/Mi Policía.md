# Mi policía
#### Fecha de análisis:
Análisis estático: 11 abril 2022   
Análisis dinámico OpenVPN: 12 abril 2022    
Análisis Posteriores:    

**Link:** https://play.google.com/store/apps/details?id=com.moobky.MiPolicia&hl=es_MX&gl=US   
**Descargas:** 500,000+   
**Fecha de actualización:** 9 abril 2022   

## Descripción de la aplicación
**Versión:** 3.0.2   
**Desarrollador:** https://www.ssc.cdmx.gob.mx/  
**Firma:** Saul Espinosa Ruiz   
**Contacto:** mipolicia@ssp.df.gob.mx  
**Condiciones de uso y Política de privacidad:**
- https://www.ssc.cdmx.gob.mx/ciudadania/mi-policia/condiciones-de-uso-y-aviso-de-privacidad  

**Uso según la playstore:**   
*La Policía de la Ciudad de México, ofrece una estrategia operativa, denominada “Cuadrantes”, orientada a lograr una mayor eficiencia del personal y cercanía con los ciudadanos, y que representa al mismo tiempo la fase final en el proceso de reestructuración integral.*

*Es así cómo se crea "Mi Policía", aplicación que acerca al ciudadano de manera interactiva a la información de su respectivo Cuadrante, proporcionando una manera rápida de hacer un llamado en caso de emergencia y conocer gráficamente la ubicación de los Cuadrantes de la Ciudad de México.*   

## Trackers (Análisis a través de Exodus Privacy)   
Esta aplicación no contiene trackers.

## Permisos   

### Permisos según la PlayStore:   
Esta aplicación tiene acceso a:   

Cámara

    Tomar fotografías y grabar videos

Teléfono

    Llamar directamente a números de teléfono

Almacenamiento

    Modificar o eliminar el contenido del almacenamiento USB
    Leer el contenido del dispositivo USB

Ubicación

    Ubicación aproximada (según la red)
    Ubicación precisa (según el GPS y la red)

Fotos/datos multimedia/archivos

    Modificar o eliminar el contenido del almacenamiento USB
    Leer el contenido del dispositivo USB

Otro

    Vincular con dispositivos Bluetooth
    Ver conexiones de red
    Controlar linterna
    Acceso completo a la red

### Permisos según Exodus Privacy

ACCESS_BACKGROUND_LOCATION

ACCESS_COARSE_LOCATION   
*Access approximate location (network-based)*

ACCESS_FINE_LOCATION   
*Access precise location (GPS and network-based)*

ACCESS_NETWORK_STATE   
*View network connections*

CALL_PHONE   
*Directly call phone numbers*

CAMERA   
*Take pictures and videos*

FLASHLIGHT

FOREGROUND_SERVICE   
*Run foreground service*

INTERNET   
*Have full network access*

### Permisos solicitados durante el uso de la aplicación
- Acceso ubicación (!)   
- Acceso a llamadas telefónicas (Si se quiere usar esta función)
- Acceso a cámara (Para escanear el número de placa del policía)
- Acceso a Whatsapp (Sección Policía Turística)
## Datos

### Datos solicitados al usuario durante el uso:
- Para los reportes de Asistencia ciudadana:
      Nombre (!)
      Apellido
      Número de contacto (!)
      Correo Electrónico

### Datos de análisis dinámico con OpenVPN:
| Dirección IP    | Número de Paquetes | País          | Ciudad/Zona | Número AS | Organización AS       |
|-----------------|--------------------|---------------|-------------|-----------|-----------------------|
| 52.36.74.154    |                 25 | United States | Boardman    |     16509 | AMAZON-02             |
| 52.38.74.42     |                  6 | United States | Boardman    |     16509 | AMAZON-02             |
| 52.88.155.1     |                 22 | United States | Boardman    |     16509 | AMAZON-02             |
| 52.89.181.193   |                 19 | United States | Boardman    |     16509 | AMAZON-02             |
| 104.110.129.127 |                 25 | United States | Los Angeles |     16625 | AKAMAI-AS             |
| 142.250.72.138  |                 20 | United States |             |     15169 | GOOGLE                |
| 142.250.101.188 |                  8 | United States |             |     15169 | GOOGLE                |
| 142.250.188.227 |                 15 | United States |             |     15169 | GOOGLE                |
| 142.250.189.10  |                 38 | United States |             |     15169 | GOOGLE                |
| 142.250.207.67  |                 27 | United States |             |     15169 | GOOGLE                |
| 142.250.217.138 |                 44 | United States |             |     15169 | GOOGLE                |
| 172.217.14.78   |               2809 | United States |             |     15169 | GOOGLE                |
| 172.217.14.110  |                 13 | United States |             |     15169 | GOOGLE                |
| 187.207.40.94   |              56584 | Mexico        | Tlalpan     |      8151 | Uninet S.A. de C.V.   |
| 189.240.234.174 |              15858 | Mexico        | Mexico City |      8151 | Uninet S.A. de C.V.   |
| 201.140.100.130 |                145 | Mexico        | Tepic       |     18734 | Operbes, S.A. de C.V. |
| 201.140.100.131 |                 52 | Mexico        | Tepic       |     18734 | Operbes, S.A. de C.V. |
| 201.140.100.136 |                 82 | Mexico        | Tepic       |     18734 | Operbes, S.A. de C.V. |
| 201.140.100.138 |                 20 | Mexico        | Tepic       |     18734 | Operbes, S.A. de C.V. |
| 216.239.32.3    |                 17 | United States |             |     15169 | GOOGLE                |

### Otros datos y trackers:

De la tabla anterior, sabemos lo siguiente:
- Los servidores de Amazon contactados, son Host de una empresa llamada [Here](https://www.here.com/). Esta empresa, entre otras cosas, desarrolla una API que permite buscar lugares y dar información al respecto. En esta app eso es usado para la función "Localizar tu cuadrante". Por la [documentación pública](https://developer.here.com/documentation/geocoder/dev_guide/topics/example-reverse-geocoding.html), sabemos que este servicio recolecta: el país, estado, ciudad, distrito, calle y código postal, así como las coordenadas exactas de localización.
- Los servidores de Google contactados son necesarios para el funcionamiento de la aplicación. Recopilan información mínima y básica de funcionamiento.
- Los servidores de Operbes se corresponden con la funcionalidad de "Asistencia Ciudadana", que sirve para hacer denuncias.
- En los servidores de Uninet están guardados tanto el vídeo del alcoholímetro, como el PDF con el reglamento de tránsito.
- El servidor de Akamai está directamente relacionado con el servicio de Here, y de ahí se extraen íconos y visuales.

### Notas

- La función de denuncia ciudadana no funcionó.
- No hemos probado el escáner de placa policial en vivo
- Para el uso de la app hay que aceptar los Términos y Condiones de Uso junto con la Política de Privacidad de manera expresa.
- La opción Agenda de movilizaciones no funciona todavía.
- Mientras la app está en uso, está activado el acceso a la ubicación en segundo plano.

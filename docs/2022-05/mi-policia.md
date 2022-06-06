# Mi policía

## Fechas de análisis

- **Análisis estático (mediante Exodus Privacy):** 11 abril 2022
- **Análisis dinámico (mediante análisis de tráfico de red):** 12 abril 2022
- **Análisis Posteriores:** -

## Descripción de la aplicación

- **Tipo:** Aplicación de emergencias de la CDMX   
- **Costo:** Gratuito   
- **Link de descarga:** [https://play.google.com/store/apps/details?id=com.moobky.MiPolicia&hl=es_MX&gl=US](https://play.google.com/store/apps/details?id=com.moobky.MiPolicia&hl=es_MX&gl=US)
- **Descargas:** 500,000+
- **Ultima fecha de actualización:** 9 abril 2022
- **Versión:** 3.0.2
- **Desarrollador:** [https://www.ssc.cdmx.gob.mx/](https://www.ssc.cdmx.gob.mx/)
- **Firma:** Saul Espinosa Ruiz
- **Contacto:** mipolicia@ssp.df.gob.mx
- **Condiciones de uso y Política de privacidad:**
    - [https://www.ssc.cdmx.gob.mx/ciudadania/mi-policia/condiciones-de-uso-y-aviso-de-privacidad](https://www.ssc.cdmx.gob.mx/ciudadania/mi-policia/condiciones-de-uso-y-aviso-de-privacidad)
- **Descripción en PlayStore:**
~~~
La Policía de la Ciudad de México, ofrece una estrategia operativa, denominada
“Cuadrantes”, orientada a lograr una mayor eficiencia del personal y cercanía
con los ciudadanos, y que representa al mismo tiempo la fase final en el proceso
de reestructuración integral.
Es así cómo se crea "Mi Policía", aplicación que acerca al ciudadano de manera
interactiva a la información de su respectivo Cuadrante, proporcionando una manera
rápida de hacer un llamado en caso de emergencia y conocer gráficamente la
ubicación de los Cuadrantes de la Ciudad de México.   
~~~

## Trackers identificados (mediante Exodus Privacy)

- **Esta aplicación no contiene trackers.**

Enlace al [reporte](https://reports.exodus-privacy.eu.org/es/reports/com.moobky.MiPolicia/latest/)   

## Empresas relacionadas con esta aplicación

- Google (Se envía información necesaria para el funcionamiento de la app, un ejemplo son conexiones a Playstore Google Services)
- Uninet (Servidor donde está albergada documentación de la app)
- Operbes (Se usa para hacer las *Denuncias ciudadanas*)
- Amazon (Para la funcionalidad de Ubicación, está relacionada con la empresa Here)
- Akamai (Se extraen visuales para los mapas)


## Permisos   

- **Según la Playstore:** 9 permisos, de los cuales 3 tienen dos subpermisos cada uno.
- **Según Exodus Privacy:** 9 permisos.
- **Según prueba de uso:** 3 permisos que se piden de manera explícita.

*Consideramos un subpermiso a aquel que se autoriza de manera secundaria al permitir otro permiso. Ejemplo, si permites acceso a tu red y en consecuencia tambien se da acceso a tu ubicación por red.*

### Permisos según la PlayStore   

- ![imagen](https://user-images.githubusercontent.com/102829552/165648944-144b0d59-f94f-4919-bf53-bb43dae4d448.png)
Ubicación
    - Ubicación aproximada (según la red)
    - Ubicación precisa (según el GPS y la red)
- ![imagen](https://user-images.githubusercontent.com/102829552/165648984-56b0e31d-0d6a-4df4-ac1d-e1395108b2c2.png)
Fotos/datos multimedia/archivos
    - Modificar o eliminar el contenido del almacenamiento USB
    - Leer el contenido del dispositivo USB
- ![imagen](https://user-images.githubusercontent.com/102829552/165649002-61b19202-91a7-4078-8371-51c292d2bb65.png)
Almacenamiento
    - Modificar o eliminar el contenido del almacenamiento USB
    - Leer el contenido del dispositivo USB
- ![imagen](https://user-images.githubusercontent.com/102829552/165649031-08fb55ba-07d2-4fae-a655-1ba91f5a2196.png)
Cámara
    - Tomar fotografías y grabar videos
- ![imagen](https://user-images.githubusercontent.com/102829552/165649048-74dc15ad-5c80-45ad-b13d-f9afdcb349e4.png)
Teléfono
    - Llamar directamente a números de teléfono



- ❔Otro
    - Vincular con dispositivos Bluetooth
    - Ver conexiones de red
    - Controlar linterna
    - Acceso completo a la red

### Permisos según Exodus Privacy

- ACCESS_BACKGROUND_LOCATION
- ![imagen](https://user-images.githubusercontent.com/102829552/165648633-88b7042c-4513-47c3-ae17-4388c8868c67.png):exclamation:
ACCESS_COARSE_LOCATION
    - *Access approximate location (network-based)*
- ![imagen](https://user-images.githubusercontent.com/102829552/165648645-f278bdda-f6a2-4eb9-9552-9ef31eb4959c.png):exclamation:
ACCESS_FINE_LOCATION   
    - *Access precise location (GPS and network-based)*
- ACCESS_NETWORK_STATE
    - *View network connections*
- ![imagen](https://user-images.githubusercontent.com/102829552/165648673-60d748f0-d68a-4d0d-89fd-81a91f1e1b55.png):exclamation:
CALL_PHONE
    - *Directly call phone numbers*
- ![imagen](https://user-images.githubusercontent.com/102829552/165648692-d271f923-a0bf-447c-ba49-4e49af730a75.png):exclamation:
CAMERA
    - *Take pictures and videos*
- FLASHLIGHT
- FOREGROUND_SERVICE
    - *Run foreground service*
- INTERNET
    - *Have full network access*

El icono :exclamation: indica un nivel 'Peligroso' o 'Especial' de acuerdo a los [niveles de protección de Google](https://developer.android.com/guide/topics/permissions/overview).

### Permisos solicitados durante el uso de la aplicación

- 🔴 Acceso ubicación (para la función botón de pánico)
- 🔵 Acceso a llamadas telefónicas (para realizar llamadas desde la aplicación)
- 🔵 Acceso a cámara (para escanear el número de placa del policía)
- *Puede acceder a Whatsapp para la *Sección Policía Turística. Aunque esto como tal no es un permiso*

🔴 Este ícono indica un permiso obligatorio   
🔵 Este ícono indica un permiso opcional pero se pierde una funcionalidad particular

## Datos

### Datos solicitados al usuario durante el uso de la aplicación

- ⚪ Para los reportes de Asistencia ciudadana:
    - 🔴 Nombre 🚨
    - ⚪ Apellido
    - 🔴 Número de contacto 🚨
    - ⚪ Correo Electrónico

🔴 Este ícono indica que se debe ingresar este dato de manera obligatoria.   
⚪ Este ícono indica que estos datos son opcionales.


### Tabla de conexiones realizadas durante el uso de la aplicación

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
| 189.240.234.174 |              15858 | Mexico        | Mexico City |      8151 | Uninet S.A. de C.V.   |
| 201.140.100.130 |                145 | Mexico        | Tepic       |     18734 | Operbes, S.A. de C.V. |
| 201.140.100.131 |                 52 | Mexico        | Tepic       |     18734 | Operbes, S.A. de C.V. |
| 201.140.100.136 |                 82 | Mexico        | Tepic       |     18734 | Operbes, S.A. de C.V. |
| 201.140.100.138 |                 20 | Mexico        | Tepic       |     18734 | Operbes, S.A. de C.V. |
| 216.239.32.3    |                 17 | United States |             |     15169 | GOOGLE                |

### Mapa de conexiones realizadas durante el uso de la aplicación

*Pendiente*

### Notas sobre datos recolectados

- Los servidores de Amazon contactados, son _Host_ de una empresa llamada [Here](https://www.here.com/). Esta empresa, entre otras cosas, desarrolla una API que permite buscar lugares y dar información al respecto. En esta app eso es usado para la función *Localizar tu cuadrante*. Por la [documentación pública](https://developer.here.com/documentation/geocoder/dev_guide/topics/example-reverse-geocoding.html), sabemos que este servicio recolecta:
    - País
    - Estado
    - Ciudad
    - Distrito
    - Calle
    - Código postal
    - Coordenadas exactas de localización
- Los servidores de Google contactados son necesarios para el funcionamiento de la aplicación. Recopilan información mínima y básica de funcionamiento.
- Los servidores de Operbes se corresponden con la funcionalidad de búsqueda de policias y sus placas y empresas privadas. Además con el corralón.
- En los servidores de Uninet están guardados tanto el vídeo del alcoholímetro, como el PDF con el reglamento de tránsito. Se usa además para la denuncia ciudadana. Es el servidor de la Secretaría de Seguridad Ciudadana.
- El servidor de Akamai está directamente relacionado con el servicio de Here, y de ahí se extraen íconos y visuales.

## Tabla de relación entre permisos y funciones

| Permisos  | Funciones relacionadas  |
|---|---|
| ACCESS_BACKGROUND_LOCATION  | Servicio de ubicación  |
| ACCESS_COARSE_LOCATION  | Servicio de ubicación  |
| ACCESS_FINE_LOCATION  | Servicio de ubicación  |
| CALL_PHONE  | Llamadas a los diferentes servicios (policía turística, cunetahabientes, etc.)   |
| CAMERA  | Escaneo de placa policial  |
| FLASHLIGHT  | Escaneo de placa policial  |
| FOREGROUND_SERVICE  | Botón de pánico  |
| INTERNET  | Internet  |

### Funciones específicas de la aplicación

- Escaneo de placa de un policía para ver si tiene derecho a levantar infracciones de tránsito
- Revisar por nombre o número de placa si un policía tiene el derecho a levantar infracciones de tránsito
- Video explicativo sobre el funcionamiento del Alcoholímetro e información general
- Denuncias de *Asistencia Ciudadana*
- Contacto con policía turística
- PDF con el reglamento de tránsito
- Se puede revisar si un vehículo se encuentra en el corralón
- Se puede comprobar si una empresa de Seguridad Privada está inscrita en el padrón de la CDMX
- Acompañamiento a cuentahabientes
- Buscar el cuadrante policial que le corresponde a uno según la dirección ingresada
- Teléfono a la unidad de contacto del Secretario de Seguridad Pública de la CDMX

## Notas

- La función de denuncia ciudadana no funcionó.
- No hemos probado el escáner de placa policial en vivo.
- La opción *Agenda de movilizaciones* descarga un PDF con la información del día.
- Mientras la app está en uso, está activado el acceso a la ubicación en segundo plano.

## Conclusiones

- Aplaudimos que sea la única aplicación analizada que no contiene trackers.
- La relación entre permisos y funciones es exacta y tiene, en general pocos permisos en comparación con las funciones que tiene. Lo que nos hace creer que la implementación de los desarrolladores es particularmente buena en comparación con las otras aplicaciones.
- Los permisos de la PlayStore no tienen una correlación directa con los encontrados por Exodus Privacy lo que no es alarmante, ya que los permisos en el código son menores a los que dice la PlayStore.

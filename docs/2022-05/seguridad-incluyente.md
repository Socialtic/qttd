# Seguridad Incluyente

## Fecha de análisis

- **Análisis estático (mediante Exodus Privacy):** 12 abril 2022    
- **Análisis dinámico (mediante captura de tráfico de red):** 18 abril 2022    
- **Análisis posteriores:**    

## Descripción de la aplicación

- **Tipo:** Emergencias estado de Puebla   
- **Costo:** Gratis   
- **Link:** [https://play.google.com/store/apps/details?id=net.garagecoders.deri](https://play.google.com/store/apps/details?id=net.garagecoders.deri)       
- **Descargas:** 50,000+  
- **Fecha de actualización:** 19 Junio 2021
- **Versión:**  1.2.4.1  
- **Desarrollador:**  [http://200.92.215.35/](http://200.92.215.35/)    
- **Firma:**  [Garage Coders](https://www.garagecoders.net/)       
- **Contacto:**  magdalena.cuellar@pueblaciudadincluyente.gob.mx   
- **Condiciones de uso y Política de privacidad:**  
  - [https://gobiernoabierto.pueblacapital.gob.mx/avisos-de-privacidad/secretaria-de-seguridad-ciudadana/item/download/22003_a78fe1764c8000f8fc4e6354ac442e3e](https://gobiernoabierto.pueblacapital.gob.mx/avisos-de-privacidad/secretaria-de-seguridad-ciudadana/item/download/22003_a78fe1764c8000f8fc4e6354ac442e3e)

- **Descripción en la PlayStore:**       
~~~
Aplicación de la Secretaría de Seguridad Ciudadana (SSC) del Municipio de Puebla, destinada a
brindar atención oportuna ante situaciones que pongan en riesgo la integridad o patrimonio de las
personas. Como parte de la Estrategia de Vectores de Proximidad, la ciudadanía podrá solicitar el
apoyo de la Policía Municipal mediante la activación de un botón virtual y observará en tiempo real
el arribo de la unidad, al lugar indicado, en un lapso no mayor a los cinco minutos. También, el
usuario podrá comunicarse, vía telefónica, con el Policía de Vector más cercano a su ubicación,
mismo que dará respuesta inmediata ante cualquier solicitud emitida. Esta aplicación brindará además
los siguientes servicios:
- Verificación de estatus de unidades ingresadas al Depósito Vehicular del Municipio.
- Acceso al tabulador de tarifas por faltas al Reglamento de Tránsito, Movilidad y Seguridad Vial.
- Servicio de atención telefónica, disponible las 24 horas, para resolver dudas sobre faltas al
Reglamento de Tránsito, Movilidad y Seguridad Vial.
- Ingreso al portal oficial de la Secretaría de Seguridad Ciudadana (SSC) que, a su vez cuenta con
información de interés para el turista.
- Emisión de felicitaciones o quejas sobre el actuar policial, mismas que serán recibidas por la
Dirección de Asuntos Internos de la corporación.

El Gobierno Municipal pone a disposición de las familias esta herramienta tecnológica, con la
finalidad de fortalecer acciones enfocadas a la prevención del delito y la construcción de entornos
más seguros.
~~~

## Trackers identificados (mediante Exodus Privacy)

- [Google Firebase Analytics](https://firebase.google.com/products/analytics)   
- [Google Crashlytics](https://firebase.google.com/products/crashlytics/)

## Empresas relacionadas con esta aplicación

- Google (Trackers y ubicación)
- Radiomovil Dipsa (Servidor donde está guardada la aplicación)
- Twitter (Presente en la página web (la aplicación actúa como explorador) del aviso de privacidad)
- Facebook (Presente en la página web (la aplicación actúa como explorador) del aviso de privacidad)
- Cloudflarenet (presente en la página de seguridad ciudadana (la aplicación actúa como explorador))
- Megacable (presente en la página de seguridad ciudadana (la aplicación actúa como explorador))
- Sucuri-sec ((Presente en la página web (la aplicación actúa como explorador) del aviso de privacidad)
- Akamai (No sabemos, probablemente actúa como CDN)
- Edgecast (No sabemos)

Enlace al [reporte](https://reports.exodus-privacy.eu.org/es/reports/net.garagecoders.deri/latest/).

## Permisos

- **Según la Playstore:** 6 permisos.   
- **Según Exodus Privacy:** 8 permisos.   
- **Según prueba de uso:** 1 permisos que se piden de manera explícita.   


### Permisos según la PlayStore

Esta aplicación puede acceder a:   

- ![imagen](https://user-images.githubusercontent.com/102829552/165636531-601a9181-224f-4192-a993-12cfa6edfeae.png)
Ubicación

    - Ubicación precisa (basada en red y GPS)


- ❔Otro motivo

    - Recibir datos de Internet
    - Ver conexiones de red
    - Acceso completo a red
    - Ejecutarse al inicio
    - Impedir que el dispositivo entre en modo de suspensión

### Permisos según Exodus Privacy

- ![imagen](https://user-images.githubusercontent.com/102829552/165636593-7837b2e7-38c5-46b1-9be8-6df060c5ee0c.png):exclamation:
ACCESS_FINE_LOCATION   
_Access precise location (GPS and network-based)_

- ACCESS_NETWORK_STATE   
_View network connections_

- FOREGROUND_SERVICE   
_Run foreground service_

- INTERNET   
_Have full network access_

- RECEIVE_BOOT_COMPLETED   
_Run at startup_

- WAKE_LOCK   
_Prevent phone from sleeping_

- RECEIVE   

- BIND_GET_INSTALL_REFERRER_SERVICE   


### Permisos solicitados al usuario durante el uso de la aplicación

- 🔴 Ubicación (Para el botón de pánico. Se recopila, según la documentación de la aplicación, aunque la app no se esté usando durante la incidencia reportada)   

🔴 Este ícono indica un permiso obligatorio


## Datos

### Datos solicitados al usuario durante el uso de la aplicación

- 🔴 Nombre (!)
- 🔴 Apellido Paterno (!)
- ⚪ Apellido Materno
- 🔴 Correo Electrónico (!)
- ⚪ Dirección
- ⚪ Capacidad auditiva (CheckBox)
Cuando se marca la checkbox de discapacidad auditiva, permite agregar un contacto de emergencia:
  - 🔴 Nombre (!)
  - 🔴 Apellido Paterno (!)
  - 🔴 Teléfono (!)
  - ⚪ Dirección

🔴 Este ícono indica que se debe ingresar este dato de manera obligatoria.   
⚪ Este ícono indica que estos datos son opcionales.   

### Tabla de conexiones realizadas durante el uso de la Aplicación

| Dirección IP    | Número de paquetes | País          | Ciudad             | Número AS | Organización AS                |
|-----------------|--------------------|---------------|--------------------|-----------|--------------------------------|
| 72.247.96.120   |                312 | United States | Los Angeles        |     16625 | AKAMAI-AS                      |
| 104.16.87.20    |                 61 |               |                    |     13335 | CLOUDFLARENET                  |
| 104.244.42.72   |                 74 | United States |                    |     13414 | TWITTER                        |
| 142.250.68.42   |                  1 | United States |                    |     15169 | GOOGLE                         |
| 142.250.72.138  |                 58 | United States |                    |     15169 | GOOGLE                         |
| 142.250.72.142  |                  6 | United States |                    |     15169 | GOOGLE                         |
| 142.250.72.170  |                 71 | United States |                    |     15169 | GOOGLE                         |
| 142.250.72.174  |                644 | United States |                    |     15169 | GOOGLE                         |
| 142.250.72.232  |                 58 | United States |                    |     15169 | GOOGLE                         |
| 142.250.72.234  |                115 | United States |                    |     15169 | GOOGLE                         |
| 142.250.141.188 |                  4 | United States |                    |     15169 | GOOGLE                         |
| 142.250.176.3   |                120 | United States |                    |     15169 | GOOGLE                         |
| 142.250.176.4   |               1334 | United States |                    |     15169 | GOOGLE                         |
| 142.250.188.227 |                106 | United States |                    |     15169 | GOOGLE                         |
| 142.250.188.238 |               1112 | United States |                    |     15169 | GOOGLE                         |
| 142.250.189.3   |                131 | United States |                    |     15169 | GOOGLE                         |
| 142.250.189.13  |                 87 | United States |                    |     15169 | GOOGLE                         |
| 142.251.34.234  |                  9 | United States |                    |     15169 | GOOGLE                         |
| 142.251.40.35   |                461 | United States |                    |     15169 | GOOGLE                         |
| 142.251.40.46   |                480 | United States |                    |     15169 | GOOGLE                         |
| 157.240.11.22   |                204 | United States | Los Angeles        |     32934 | FACEBOOK                       |
| 157.240.11.35   |                103 | United States | Los Angeles        |     32934 | FACEBOOK                       |
| 172.217.14.106  |                544 | United States |                    |     15169 | GOOGLE                         |
| 187.216.248.254 |                175 | Mexico        | San Andres Cholula |     28403 | RadioMovil Dipsa, S.A. de C.V. |
| 189.199.68.17   |               2192 | Mexico        | Puebla City        |    262916 | Mega Cable, S.A. de C.V.       |
| 192.124.249.31  |                 12 | United States | Menifee            |     30148 | SUCURI-SEC                     |
| 192.124.249.36  |                 11 | United States | Menifee            |     30148 | SUCURI-SEC                     |
| 192.229.163.25  |                103 | United States |                    |     15133 | EDGECAST                       |
| 200.92.215.35   |                366 | Mexico        | Puebla City        |     13999 | Mega Cable, S.A. de C.V.       |
| 216.239.32.3    |                 78 | United States |                    |     15169 | GOOGLE                         |

### Mapa de conexiones

### Notas sobre datos recolectados

- La aplicación contacta a los servidores de google por tres razones: los mapas y la geolocalización; el archivo PDF de "Tabulador de multas e infracciones"; y por el tracker de Firebase (que incorpora el de Crashlytics). El tracker de Firebase, asigna través de [firebaseinstallations](https://firebase.google.com/docs/reference/android/com/google/firebase/installations/FirebaseInstallations), una id particular a la instalación de la app. De ahí recolecta, a través de app-measurement.com toda una serie de eventos realizados en la aplicación. Aquí los enlaces a todos los eventos y datos que, de manera estándar se recolectan [1](https://support.google.com/firebase/answer/9234069?hl=en&ref_topic=6317484&visit_id=637859685880636053-1936242821&rd=1), [2](https://support.google.com/firebase/answer/9268042?hl=en&ref_topic=6317484&visit_id=637859685880636053-1936242821&rd=1), [3](https://support.google.com/firebase/answer/7029846?hl=en&ref_topic=7029512).
- Las conexiones a Twitter y Facebook son trackers que tienen que ver con la página de información del aviso de Privacidad (En la cual no se muestra el aviso).
- El servidor de Cloudflare está relacionado con la página en construcción de la Secretaría de seguridad ciudadana.
- Los mensajes de quejas y felicitaciones van al servidor de RadioMóvil Dipsa, a esta [página](https://deridev.com/auth/login). También la función sobre revisar si un coche está en el corralón dirige a este servidor.
- El servidor de RadioMóvil Dipasa es el _Host_ de la aplicación. Ahí se guardan todos los datos de registro.
- Las conexiones a [Sucuri-sec](https://sucuri.net/) son llamadas en HTTP. Es un servicio que revisa que las páginas web no tengan malware y estén seguras. Es prudente suponer que estas conexiones tienen que ver con la misma página del aviso de privacidad.
- La conexión a Mega Cable es la página (en construcción) de la Secretaría de Seguridad Ciudadana. Esta conexión está en HTTP.

## Tabla de relación entre permisos y funciones

| Permisos  | Funciones relacionadas  |
|---|---|
| ACCESS_FINE_LOCATION  | Servicio de ubicación  |
| ACCESS_NETWORK_STATE  | Internet  |
| FOREGROUND_SERVICE  | Botón de pánico  |
| INTERNET  | Internet  |
| RECEIVE_BOOT_COMPLETED  | No sabemos para qué  |
| WAKE_LOCK  | Botón de pánico  |
| RECEIVE  | Push Notifications  |
| BIND_GET_INSTALL_REFERRER_SERVICE  | Tracker Firebase  |

### Funciones específicas de la aplicación

- Se puede revisar si un coche se encuentra en el corralón
- Se pueden mandar quejas, sugerencias y felicitaciones a la Policía
- Tiene las siguientes funciones que abren la instancia de llamada en Android:
  - Acompañamiento Bancario
  - Dudas sobre Infracciones
  - Grúa
- Página con dirección del Ayuntamiento de Puebla y otros datos.
- Consulta del tabulador de Infracciones

## Notas

- El link provisto por la PlayStore a la política de privacidad no es el correcto. Lo mismo con la redirección al aviso de privacidad dentro de la aplicación.
- Botón de auxilio no sirve por estar fuera de Puebla.

## Conclusiones

- La relación entre permisos y funciones es simétrica con excepción del permiso _receive_boot_completed_ que permite que una aplicación se inicie de manera automática cuando se reinicia el teléfono, cosa que no sucede con esta app.
- No tiene problemas flagrantes de seguridad.
- Lo que nos preocupa un poco es que da acceso a varias páginas que tienen trackers de Facebook y Twitter. Páginas que, además que no deberían tener esos trackers ya que son del gobierno del estado de Puebla, pueden hacer que un usuario sea rastreado en su móvil al utilizar esta aplicación.
- Tiene dos trackers, Firebase y su subtracker Firebase Analytics. Si bien, en el mejor de los casos, no deberían estar, tampoco es una aplicación que presenta trackers en exceso.

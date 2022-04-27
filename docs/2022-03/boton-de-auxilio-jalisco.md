# Botón de Auxilio Jalisco
#### Fecha de análisis:
Análisis estático (mediante Exodus Privacy): 12 abril 2022    
Análisis dinámico (mediante análisis de tráfico de red): 18 abril 2022  
Análisis posteriores:    

## Descripción de la aplicación:
**Link:** [https://play.google.com/store/apps/details?id=com.jpriskcorp.botonpanicoapp.jal](https://play.google.com/store/apps/details?id=com.jpriskcorp.botonpanicoapp.jal)      
**Descargas:** 50,000+  
**Fecha de actualización:** 13 Enero 2022
**Versión:**  94
**Desarrollador:**  [https://c5jalisco.gob.mx/](https://c5jalisco.gob.mx/)  
**Firma:**  riskcorp@yahoo.com.mx/C=US     
**Contacto:**  operativaceinco@gmail.com   
**Condiciones de uso y Política de privacidad:**  
- [https://fge.jalisco.gob.mx/content/terminos-y-politicas-boton-de-panico](https://fge.jalisco.gob.mx/content/terminos-y-politicas-boton-de-panico)  

**Descripción en PlayStore**
~~~
El Botón de Auxilio Jalisco es una aplicación para smartphones del Estado de Jalisco que
permite que el usuario registrado pueda enviar una alerta inmediata al Centro de Coordinación,
Comando, Control, Comunicaciones, y Cómputo del Estado de Jalisco (Escudo Urbano C5 Jalisco).

La aplicación envía directamente la alerta al Escudo Urbano C5, en donde personal calificado recibe
el caso y efectúa todos los pasos establecidos para dar curso a la situación y resolver el problema
de manera rápida y efectiva.

Recuerde en casos de emergencia se sugiere llamar a la línea 9-1-1. En caso que esto no sea posible,
esta aplicación surge como una vía alternativa de contacto con las autoridades para denunciar un
caso de emergencia. Tan sólo presionando el botón de pánico sus datos previamente registrados en el
sistema y su geolocalización son enviadas automáticamente al Escudo Urbano C5.
Utiliza esta aplicación con responsabilidad.
~~~       

## Trackers identificados (mediante Exodus Privacy)
- [Google Admob](https://admob.google.com/home/)  
- [Google Analytics](https://marketingplatform.google.com/about/analytics/)   
- [Google Crashlytics](https://firebase.google.com/products/crashlytics/)   
- [Google Firebase Analytics](https://firebase.google.com/)   
- [Google Tag Manager](https://marketingplatform.google.com/about/tag-manager/)

Enlace al [reporte](https://reports.exodus-privacy.eu.org/es/reports/com.jpriskcorp.botonpanicoapp.jal/latest/).

## Permisos

- **Según la Playstore:** 12 permisos, de los cuales 4 tienen dos subpermisos cada uno.
- **Según Exodus Privacy:** 15 permisos.
- **Según prueba de uso:** 5 permisos que se piden de manera explícita.

#### Permisos según la PlayStore:
Esta aplicación puede acceder a:   

- ![imagen](https://user-images.githubusercontent.com/102829552/165629344-e744820c-f52d-4359-8238-ee3e3d1494b1.png)
Contactos

    - Consultar tus contactos


- ![imagen](https://user-images.githubusercontent.com/102829552/165629369-d867e558-7e41-41ad-905c-4bbd24597e41.png)
Ubicación

    - Ubicación aproximada (basada en red)
    - Ubicación precisa (basada en red y GPS)


- ![imagen](https://user-images.githubusercontent.com/102829552/165629391-9c779048-f477-4a4e-8155-d294f78daf7a.png)
Teléfono

    - Llamar directamente a números de teléfono
    - Consultar la identidad y el estado del teléfono


- ![imagen](https://user-images.githubusercontent.com/102829552/165629423-307f26bf-db54-459c-bbb4-50a58a0dd9a9.png)
Fotos/multimedia/archivos

    - Leer el contenido de tu almacenamiento USB
    - Modificar o eliminar contenido del almacenamiento USB


- ![imagen](https://user-images.githubusercontent.com/102829552/165629440-2f7ca69b-d9ff-4f31-a627-ff03c2ad917f.png)
Almacenamiento

    - Leer el contenido de tu almacenamiento USB
    - Modificar o eliminar contenido del almacenamiento USB


- ![imagen](https://user-images.githubusercontent.com/102829552/165629468-d1fb02c1-f4ef-45c8-b316-fb5c1c420f04.png)
ID de dispositivo e información de llamada

    - Consultar la identidad y el estado del teléfono


- ❔ Otro

    - Recibir datos de Internet
    - Ver conexiones de red
    - Acceso completo a red
    - Controlar la vibración
    - Impedir que el dispositivo entre en modo de suspensión
    - Leer la configuración de los servicios de Google

#### Permisos según Exodus Privacy:

- ![imagen](https://user-images.githubusercontent.com/102829552/165629714-c564c696-d04f-481e-ab77-925c3cf74017.png):exclamation:
ACCESS_COARSE_LOCATION   
_Access approximate location (network-based)_

- ![imagen](https://user-images.githubusercontent.com/102829552/165629745-d1c2e269-035c-4658-af7b-e5ce9ee36e75.png):exclamation:
ACCESS_FINE_LOCATION   
_Access precise location (GPS and network-based)_

- ACCESS_NETWORK_STATE   
_View network connections_

- ![imagen](https://user-images.githubusercontent.com/102829552/165629860-bb716424-e37b-48c9-8997-220361adf096.png):exclamation:
CALL_PHONE   
_Directly call phone numbers_

- FOREGROUND_SERVICE   
_Run foreground service_

- INTERNET   
_Have full network access_

- ![imagen](https://user-images.githubusercontent.com/102829552/165629974-9e8550fc-d07d-4d06-9333-ae925b667a76.png):exclamation:
READ_CONTACTS   
_Read your contacts_

- ![imagen](https://user-images.githubusercontent.com/102829552/165629893-d3d776a8-479c-4cb8-b879-de5f80354066.png):exclamation:
READ_PHONE_STATE   
_Read phone status and identity_

- VIBRATE   
_Control vibration_

- WAKE_LOCK   
_Prevent phone from sleeping_

- ![imagen](https://user-images.githubusercontent.com/102829552/165630048-7a93b835-988c-4a7a-a46f-fb6c9022c5ff.png):exclamation:
WRITE_EXTERNAL_STORAGE   
_Modify or delete the contents of your SD card_

- RECEIVE   

- READ_GSERVICES   

- C2D_MESSAGE   

- MAPS_RECEIVE    

#### Permisos solicitados durante el uso de la aplicación:
- Acceso a Ubicación (!)
- Acceso a Contactos (!)
- Acceso a Llamadas (!)
- Acceso a Almacenamiento (!)
- Acceso a Estado del Teléfono (!)
## Datos
#### Datos solicitados al usuario durante el uso
- Nombre (!)
- Apellido Paterno (!)
- Apellido Materno
- Correo electrónico (!)
- Número de teléfono (!)
- Número de contacto (!)
- Riesgos o padecimientos
- Tipo de usuario (Incluye: particular, transporte público, transporte privado, escuela, tienda de conveniencia, nave industrial, otro).
- Puesto en caso de haber seleccionado empresa


#### Tabla de conexiones realizadas durante el uso de la aplicación
| Dirección IP    | Número de paquetes | País          | Ciudad  | Número AS | Organización AS                     |
|-----------------|--------------------|---------------|---------|-----------|-------------------------------------|
| 131.196.248.8   |                140 | Mexico        | Zapopan |    265524 | COEFICIENTE COMUNICACIONES SA DE CV |
| 142.250.68.42   |                 62 | United States |         |     15169 | GOOGLE                              |
| 142.250.68.74   |                 76 | United States |         |     15169 | GOOGLE                              |
| 142.250.72.174  |                858 | United States |         |     15169 | GOOGLE                              |
| 142.250.101.188 |                  2 | United States |         |     15169 | GOOGLE                              |
| 142.250.141.188 |                 36 | United States |         |     15169 | GOOGLE                              |
| 142.250.176.3   |                 23 | United States |         |     15169 | GOOGLE                              |
| 142.250.176.4   |                 80 | United States |         |     15169 | GOOGLE                              |
| 142.250.188.234 |                 27 | United States |         |     15169 | GOOGLE                              |
| 142.250.189.10  |                 39 | United States |         |     15169 | GOOGLE                              |
| 142.251.40.35   |                 23 | United States |         |     15169 | GOOGLE                              |
| 142.251.40.42   |               1066 | United States |         |     15169 | GOOGLE                              |
| 142.251.40.46   |                  3 | United States |         |     15169 | GOOGLE                              |
| 172.217.14.74   |                 33 | United States |         |     15169 | GOOGLE                              |


#### Otros datos recolectados
- Error: androidx.multidex.MultideDexApplication relies on google play services. Por lo tanto no hubo conexiones a Google en los trackers. Sin embargo podemos suponer que al estar Firebase, sucede lo mismo que en las otras apps.
- **El servidor de Coeficiente Comunicaciones es el host de la app. Las llamadas a ese servidor se hacen en HTTP, tanto las de emergencia como las de registro, es decir que no están cifradas.**

#### Funciones notables
- Tiene un botón "Prueba de Servicio" que permite verificar que todo funciona sin que se  haga una llamada o notificación real de emergencia.
- Incluye Auxilio Ciudadano (Policía); Bomberos; Médicos y llamada directa a 911.
- Incluye botón de acceso rápido (3 toques seguidos del botón de apagado o bloqueo). Con esto, según la documentación, se hace un aviso de emergencia de manera automática. Como la prueba se hizo fuera de Jalisco, no pudimos probar esta funcionalidad.
- Permite modificar los datos, la contraseña y darse de baja.
### Notas
- El permiso de acceso a contactos es para ingresar 3 contactos desde la libreta de Google a los que se notifica por SMS en caso de emergencia.
- El permiso de Acceso a Estado permite la funcionalidad del botón de acceso rápido
- Hay que aceptar los Términos de uso de manera expresa
- Hay que aceptar el Aviso de Privacidad de manera expresa
- Mandan un correo con un código para verificar la cuenta.
- Solicita la opción de ubicación fina en los permisos (basado en redes wifi, GPS y otros)
- Funcionalidad de ubicación proporcionado por Google.

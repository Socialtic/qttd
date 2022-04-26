# Mujeres Seguras
#### Fecha de análisis:
Análisis estático (mediante Exodus Privacy): 12 abril 2022   
Análisis dinámico (mediante análisis de tráfico de red): 18 abril 2022     
Análisis Posteriores: 19 abril 2022   

## Descripción de la aplicación
**Tipo:** Aplicación de emergencia para mujeres del estado de sonora
**Costo:** Gratuito
**Link:** [https://play.google.com/store/apps/details?id=mx.gob.segobsonora.mujersegura](https://play.google.com/store/apps/details?id=mx.gob.segobsonora.mujersegura)   
**Descargas:** 50,000+   
**Fecha de actualización:** 7 Enero 2022   
**Versión:** 2.0.0  
**Desarrollador:** [https://mujeresseguras.sonora.gob.mx/](https://mujeresseguras.sonora.gob.mx/)    
**Firma:** Android, Google Inc.   
**Contacto:** sistema.estatal@sspsonora.gob.mx  
**Condiciones de uso y Política de privacidad:**
- [https://www.sonora.gob.mx/politica-de-uso.html](https://www.sonora.gob.mx/politica-de-uso.html)

**Descripción en playstore:**   
~~~
Aplicación móvil para las mujeres con el objetivo de erradicar la violencia de género, que contiene
botón de ayuda en caso de encontrarse en riesgo dentro del Estado de Sonora.
Está conectada directamente al Centro de Control, Comando, Comunicación, Cómputo, Coordinación
e Inteligencia C5i enviando ubicación georreferenciada así como número telefónico en la cual las
autoridades acudirán de forma inmediata en auxilio. De igual manera, se notificará a la red de
confianza.

Ademas cuenta con el servicio de datos patrocinados que te permitirá utilizar el botón de alerta
aunque no cuentes con datos móviles.
~~~  

## Trackers identificados (mediante Exodus Privacy)   
- [Google Firebase Analytics](https://firebase.google.com/)  

Enlace al [reporte](https://reports.exodus-privacy.eu.org/es/reports/mx.gob.segobsonora.mujersegura/latest/).

## Permisos   

### Permisos según la PlayStore:   
Esta aplicación puede acceder a:   
- Identidad

    - Buscar cuentas en el dispositivo


- Contactos

    - Buscar cuentas en el dispositivo
    - Consultar tus contactos
    - Modificar tus contactos


- Ubicación

    - Ubicación aproximada (basada en red)
    - Ubicación precisa (basada en red y GPS)
    - Acceder a comandos de proveedor de ubicación adicional


- Teléfono

    - Llamar directamente a números de teléfono
    - Consultar la identidad y el estado del teléfono


- Fotos/multimedia/archivos

    - Leer el contenido de tu almacenamiento USB
    - Modificar o eliminar contenido del almacenamiento USB


- Almacenamiento

    - Leer el contenido de tu almacenamiento USB
    - Modificar o eliminar contenido del almacenamiento USB


- ID de dispositivo e información de llamada

    - Consultar la identidad y el estado del teléfono


- Otro motivo

    - Recibir datos de Internet
    - Ver conexiones de red
    - Crear cuentas y establecer contraseñas
    - Emparejar con dispositivos Bluetooth
    - Acceso completo a red
    - Leer la configuración de sincronización
    - Ejecutarse al inicio
    - Controlar la vibración
    - Impedir que el dispositivo entre en modo de suspensión
    - Activar y desactivar la sincronización

### Permisos según Exodus Privacy
- ACCESS_COARSE_LOCATION   
_Access approximate location (network-based)_

- ACCESS_FINE_LOCATION   
_Access precise location (GPS and network-based)_

- ACCESS_LOCATION_EXTRA_COMMANDS   
_Access extra location provider commands_

- ACCESS_NETWORK_STATE   
_View network connections_

- AUTHENTICATE_ACCOUNTS   

- BLUETOOTH   
_Pair with Bluetooth devices_

- CALL_PHONE   
_Directly call phone numbers_

- FOREGROUND_SERVICE   
_Run foreground service_

- GET_ACCOUNTS   
_Find accounts on the device_

- INTERNET   
_Have full network access_

- READ_CONTACTS   
_Read your contacts_

- READ_PHONE_STATE   
_Read phone status and identity_

- READ_SYNC_SETTINGS   
_Read sync settings_

- RECEIVE_BOOT_COMPLETED   
_Run at startup_

- VIBRATE   
_Control vibration_

- WAKE_LOCK   
_Prevent phone from sleeping_

- WRITE_CONTACTS   
_Modify your contacts_

- WRITE_EXTERNAL_STORAGE   
_Modify or delete the contents of your SD card_

- WRITE_SYNC_SETTINGS    
_Toggle sync on and off_

- RECEIVE   

- BIND_GET_INSTALL_REFERRER_SERVICE   

- ACTIVITY_RECOGNITION    


### Permisos solicitados al usuario durante el uso de la aplicación
- Acceso a Llamadas telefónicas (Para llamar a los centros del ISM)
- Acceso a Ubicación (!)
- Acceso a contactos (Para la Red de Emergencias)


## Datos

### Datos solicitados al usuario durante el uso de la aplicación
- Nombre (!)
- Apellido Paterno (!)
- Apellido Materno
- Número de teléfono (!)
- Fecha de nacimiento (!)
- Género
- Discapacidad
- Indígena o perteneciente a una etnia
- Correo Electrónico


### Tabla de conexiones realizadas durante el uso de la aplicación

| Dirección IP    | Número de paquetes | País          | Ciudad  | Número AS | Organización AS                        |
|-----------------|--------------------|---------------|---------|-----------|----------------------------------------|
| 142.250.68.10   |                 28 | United States |         |     15169 | GOOGLE                                 |
| 142.250.68.42   |                126 | United States |         |     15169 | GOOGLE                                 |
| 142.250.68.74   |                282 | United States |         |     15169 | GOOGLE                                 |
| 142.250.68.106  |                 49 | United States |         |     15169 | GOOGLE                                 |
| 142.250.72.170  |                 24 | United States |         |     15169 | GOOGLE                                 |
| 142.250.72.174  |                 29 | United States |         |     15169 | GOOGLE                                 |
| 142.250.217.138 |                 29 | United States |         |     15169 | GOOGLE                                 |
| 142.251.40.35   |                  5 | United States |         |     15169 | GOOGLE                                 |
| 142.251.40.46   |                 27 | United States |         |     15169 | GOOGLE                                 |
| 187.189.158.27  |                136 | Mexico        | Navojoa |     22884 | TOTAL PLAY TELECOMUNICACIONES SA DE CV |


### Otros datos recolectados:
- La aplicación contacta a los servidores de google por dos razones: los mapas y la geolocalización y por el tracker de Firebase. Este último asigna, a través de otro tracker, [firebaseinstallations](https://firebase.google.com/docs/reference/android/com/google/firebase/installations/FirebaseInstallations), una id particular a la instalación de la app. De ahí recolecta, a través de app-measurement.com toda una serie de eventos realizados en la aplicación. Aquí los enlaces a todos los eventos y datos que, de manera estándar se recolectan [1](https://support.google.com/firebase/answer/9234069?hl=en&ref_topic=6317484&visit_id=637859685880636053-1936242821&rd=1), [2](https://support.google.com/firebase/answer/9268042?hl=en&ref_topic=6317484&visit_id=637859685880636053-1936242821&rd=1), [3](https://support.google.com/firebase/answer/7029846?hl=en&ref_topic=7029512).

- El servidor perteneciente a Total Play, es el host de la aplicación: servicios.sspsonora.gob.mx. Todas las comunicaciones están cifradas y es en este servidor donde se procesan las alertas de pánico. Estas son enviadas en formato JSON y cuentan con ID de alerta, un número de folio y la ubicación.
- En este servidor también se guardan los contactos de emergencia en formato JSON: id de contacto, nombre y teléfono.
- En este servidor se guarda la información de contacto que proporciona el usuario.

### Funciones notables
- Tiene la función de datos patrocinados (Si la persona no tiene datos, aun así puede hacer uso de la app). No está comprobado
- Cuenta con contactos de red de confianza. Pueden ser agregados de manera manual o accediendo a la libreta de contactos de la cuenta de Google. Además estos contactos deben tener la app instalada. No está comprobado.
- Tiene una función de Falsa Alarma.
- Es opcional, pero se puede realizar una encuesta de violencia de pareja a la cual otorgan un resultado y una recomendación.
- Acceso al directorio de centros ISM (Instituto Sonorense de la Mujer).
- Acceso a un violentómetro.


### Notas

- Hay muchos permisos que no se justifican en las funciones: Bluetooth, Modificar contactos, Encontrar cuentas en el dispositivo, etc.
- La app está firmada por Google.
- La app está conectada con el C5i.
- El pin de ubicación no sirvió, probablemente por estar fuera del área de servicio.
- Hay que aceptar de manera expresa el Aviso de Privacidad (está reducido).

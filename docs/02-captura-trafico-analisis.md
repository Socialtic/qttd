# Captura y análisis del tráfico de red de cualquier aplicación en Android
En esta sección mostraremos cómo capturar los paquetes de red de un celular desde una máquina virtual para luego analizarlos. Los prerrequisitos son:
   - Cliente de WireGuard instalado en el celular y configurado. 
   - Máquina virtual con el servidor VPN WireGuard instalado.
   - El cliente y el servidor deben estár los dos en la misma red local.
      
La idea es conectar el teléfono a nuestra red privada virtual (VPN) y en esa red correr otro programa que se llama Tshark, que nos permitirá capturar el tráfico de red (los datos que envía y recibe nuestro teléfono) para luego poder analizarlos con Wireshark.

Como última nota, Tshark es la versión de línea de comandos de Wireshark. Utilizamos este programa porque resulta más rápido y cómodo para la captura de paquetes.

## Otros requerimientos 

Android es un sistema operativo de Google utilizado en teléfonos y tabletas. La versión que normalmente viene de fábrica en los dispositivos, es una versión modificada de la versión original,  y está hecha por el fabricante del dispositivo físico (Samsung, Motorla, LG, Nokia, etc.) y ulteriormente modificada por nuestro proveedor de servciio de telefonía móvil. Se supone que Android es *Open-Source* (código abierto), lo que quiere decir que cualquiera puede tener acceso al código de Android y modificarlo a su gusto. 

Hay varias comunidades de desarrolladores que han modificado las versiones de Android para hacerlas más privadas, más seguras, más rápidas, más ligeras, con otro tipo de funcionalidades y muchas cosas más. Entre ellas, una de las más conocidas y utilizadas es [LineageOS](https://lineageos.org/). Soporta varias marcas y modelos de dispositivos y es gratis. Como es bastante utilizada, hay muchos foros donde uno puede encontrar soluciones si uno se encuentra con problemas. 

Para las pruebas de las aplicaciones, nosotros hemos utilizado un celular que justamente tiene esta versión de Android instalada. Sin embargo, no es tan sencillo instalarla e implica borrar todos los datos del teléfono, además de que existe el riesgo (mínimo) de *romper* nuestro celular y dejarlo inutilizable. Idealmente, las pruebas del tráfico de aplicaciones deberían hacerse con un celular que tenga LineageOS, esto, por la simple razón de que es una versión de Android desprovista de muchísimas de las funciones y aplicaciones que el fabricante, nuestro proveedor de telefonía y el propio Google agregan a nuestros celulares. De esto resulta que la captura del tráfico de red es más limpia y es más fácil controlar qué aplicaciones se están conectando a Internet. 

Sin embargo entendemos que tener un celular con LineageOS no siempre es factible o lo más sencillo. En este sentido, otra solución puede ser desinstalar la mayoría de apps presentes en el celular e [inhabilitar](https://support.google.com/android/answer/2521768?hl=es) las que no se pueden desinstalar. También entendemos que esto sea un probelma, así que nuestra tercera opción es sencillamente quitarle a todas las apps, el permiso de acceso a internet. Dejamos aquí una [guía](https://www.digitalcitizen.life/how-block-internet-access-specific-apps-android/) para hacerlo cuando se tiene Android 10. Dejamos aquí una [guía](https://krispitech.com/how-to-prevent-android-apps-from-sending-and-receiving-data-in-background/) para Android 11. A partir de Android 12, esta opción de deshabilitar el acceso a Internet fue eliminada (o no la pudimos encontrar), y ahora sólo queda el acceso a datos en segundo plano. Esta opción también nos puede ser de utilidad, ya que, al eliminar este permiso, sólo la app que esté abierta se conectará a Internet. Ojo! Es importante, al hacerlo, marcar a cuáles apps se les quitó este permiso, para poder volver a dárselos. Hay muchas apps que necesitan acceder a datos en segundo plano para proporcionar ciertas funcionalidades, por ejemplo, Outlook o Gmail o Whatsapp, para avisar al usuario si tiene algún nuevo mensaje.  
Para quitar este permiso, ir a **Configuración** (el ícono con la rueda de engrane); **Apps**, dar click en la app deseada, luego **Wi-Fi y datos móviles** y eliminar el permiso de **Datos en segundo plano**.

## Captura de datos

- Instalar la aplicación que se quiere analizar
- Cerrar todas las aplicaciones que están corriendo
- Activar WireGuard
- En la máquina virtual, en la consola, inicializar el programa `tshark`. Para esto, el comando es:
   
   ```
   sudo tshark -i enp0s3 -w /tmp/nombredelapp.pcap
   ```
El modificador -i, le dice a Tshark a qué interfaz (i viene de *interface*) conectarse. La que nos interesa siempre va a tener el prefijo "en", ya que esto hace referencia a Ethernet, que es la manera en la cual nuestra máquina virtual se conecta a nuestra red local. Los nombres más comunes son enp0s3 y ens33.  El modificador -w (write) le indica a Tshark dónde guardar el tráfico de red capturado. Aquí utilizamos la carpeta tmp (temporal) para evitar problemas con los permisos de escritura de Linux. Poner el nombre que se quiera al archivo, sugerimos el nombre de la aplicación, y poner la extensión del archivo en .pcap (que es la extensión de los archivos que puede abrir Wireshark).

- Abrir la aplicación que queremos analizar. Si todo está bien, veremos algo similar a esto en nuestra pantalla:


El número de hasta abajo irá aumentando. Estos son los paquetes de datos que estamos capturando. 

- Explorar la aplicación e intentar utilizar todas sus funciones. Esto es importante para poder saber a todos los servidores a los que se conecta. 

- Después de explorar la aplicación, cerrarla en el celular y en la consola apretar la tecla **ctrl + c**. Esto manda la señal al programa de Tshark de detenerse.

- Si estamos contentos con nuestro archivo, podemos cambiarlo a nuestro dorectorio de documentos en la máquina virtual. Para esto hay que poner el siguiente comando

sudo chmod 777 /tmp/nombredelapp.pcap

Este comando permite que podamos mover de lugar nuestro archivo. 







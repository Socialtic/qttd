# Instalación de servidor VPN

## Prerrequisitos

1. Linux Ubuntu o Linux Mint
2. VirtualBox instalado
3. Máquina Virtual con Ubuntu Server 20.04 LTS instalado
4. El modo red de la máquina virtual debe ser "bridged" o "puente". Esto le dará a la máquina virtual una ip del estilo: 192.168.x.x. Si la ip de la máquina virtual es del estilo 10.x.x.x, se está utilizando el modo NAT y no el Bridged. Hay que cambiarlo en la sección de Configuración/Red de VirtualBox. Para averiguar la ip local basta correr el comando.

```
ip a
```

Bajo la interfaz enp0s3 debería aparecer la dirección ip.   

## Instalación OpenVPN

Bajar el siguiente script:

``` 
curl -O https://raw.githubusercontent.com/angristan/openvpn-install/master/openvpn-install.sh
```

Cambiar los permisos de ejecución del script:
``` 
chmod +x openvpn-install.sh
```

Ejecutar el script:
```
sudo bash openvpn-install.sh
```   

Si en la primera pregunta la ip es de la forma 192.168.x.x, entonces dar enter.
![imagen](https://user-images.githubusercontent.com/76178268/158869657-5d95e961-4df1-46c2-8576-ff56e48e5d52.png)

En la siguiente pregunta, el script reconocerá la ip pública, aceptar.   
![imagen](https://user-images.githubusercontent.com/76178268/158870405-d3a5b737-615b-46a6-b7d1-e19e2a2c6c58.png)

Seleccionar el puerto por default o cambiarlo:   
![imagen](https://user-images.githubusercontent.com/76178268/158870470-fdd18d07-f692-495c-8183-51f1bd8cedd7.png)

Seleccionar el protoclo UDP:   
![imagen](https://user-images.githubusercontent.com/76178268/158870526-ea563a71-c878-4e59-bb24-481d9dbc8f84.png)

Seleccionar el DNS de CloudFlare:   
![imagen](https://user-images.githubusercontent.com/76178268/158870655-4ae5c3a0-4d0d-4d88-8ee6-add79484d6d4.png)

No usar compresión:   
![imagen](https://user-images.githubusercontent.com/76178268/158870803-14e8feda-ea57-4427-a992-afec0c5fe38a.png)

No modificar las opciones cifrado:   
![imagen](https://user-images.githubusercontent.com/76178268/158870862-339763ea-ef36-499c-8806-317943851326.png)

Continuar con la instalación y si todo resultó conrrectamente, el script nos pedirá el nombre del cliente. Este nombre puede ser aleatorio.   
![imagen](https://user-images.githubusercontent.com/76178268/158871430-be19887a-dcd7-4be0-9fea-8644b03f5e32.png)

Se puede agregar un password, aunque no es necesario:   
![imagen](https://user-images.githubusercontent.com/76178268/158871658-c12ca8da-8749-4744-bd28-e04f5aa9a586.png)

Si no hay ningún error, tendremos la siguiente pantalla:   
![imagen](https://user-images.githubusercontent.com/76178268/158872001-af4de4a3-ffe9-4632-939d-3201b7a3af12.png)

Listar la carpeta /etc/openvpn/
```
ls /etc/openvpn
```

Si en dicho directorio existen muchos archivos, como se ve en la siguiente imagen:   
![imagen](https://user-images.githubusercontent.com/76178268/158872209-78ec98f4-bc8a-4f92-a0df-1cce4b7c483b.png)

Entonces es necesario mover casi todos al directorio /server. En la carpeta /etc/openvpn/ sólo deben estar los siguientes archivos y directorios:
- /ccd
- /client
- /server
- client-template.txt
- update-resolv-conf

Los demás archivos deben moverse al directorio de server.

Entramos a la carpeta /etc/openvpn:

```
cd /etc/openvpn
```

Movemos los archivos:

```
sudo mv archivo.1 archivo.2 dir.1 dir.2 /etc/openvpn/server
```

Permitimos el servicio de OpenVPN:

```
sudo systemctl enable openvpn-server@server.service
```

Reiniciamos el servidor desde el menú de VirtualBox Archivo/Cerrar/Enviar Señal de apagado.

```
sudo systemctl openvpn-server@server.service
```

Activamos el servicio openvpn-server:

```
sudo systemctl start openvpn-server@server.service
```

Revisamos que no haya problemas:

```
sudo systemctl status openvpn-server@server.service
```

Debería aparecer una pantalla similar:   
![imagen](https://user-images.githubusercontent.com/76178268/158872289-e84bb02c-db2e-484c-a9dc-b9cbd63b9dad.png)

## Instalación del servidor SSH

Para poder recuperar el archivo de cliente nombre.ovpn, necesitamos pasarlo a la máquina huésped de la máquina virtual. Hay varias maneras, aquí sugerimos una muy sencilla.

Instalamos openssh server:

```
sudo apt install openssh-server
```

Permitimos el servicio:

```
sudo systemctl enable ssh
```

Activamos el servicio:

```
sudo systemctl start ssh
```

## Recuperación y edición del archivo de cliente
En la terminal de la máquina huesped ingresamos el siguiente comando:

```
scp nombre_usuario@192.168.x.x:nombre.ovpn /home/usuario/Descargas
```

Una vez que tenemos el archivo en nuestra máquina huesped, tenemos que editarlo. Abrirlo con cualquier editor de texto y cambiar la siguiente línea por la ip local:   
![imagen](https://user-images.githubusercontent.com/76178268/158872516-ae22246f-eddd-4c6c-ae36-b7200bd9b349.png)

Guardar los cambios y enviarlo al celular.

## OpenVPN en el celular
 
Descargamos desde la Playstore la app OpenVPN:   
![imagen](https://user-images.githubusercontent.com/76178268/158872588-579f1ca6-9072-4c7c-81d7-68c9602b0a54.png)

Abrimos la app y aceptamos la licencia de uso:   
![imagen](https://user-images.githubusercontent.com/76178268/158872648-2896c061-70a4-49f1-b7cd-c15e7dc0348e.png)

Nos vamos a FILE:   
![imagen](https://user-images.githubusercontent.com/76178268/158872697-5fabfa88-b04f-44f1-a0a5-def0d1529f7b.png)

Seleccionamos la carpeta donde tenemos nuestro archivo de cliente:   
![imagen](https://user-images.githubusercontent.com/76178268/158872750-4e3f287e-153e-44c9-b8a7-395f12045222.png)

Lo seleccionamos y le damos importar:   
![imagen](https://user-images.githubusercontent.com/76178268/158872805-b444ae76-bb30-47d0-b80e-818f4a363e33.png)

Seleccionamos Connect after import, le damos en ADD y aceptamos la advertencia de seguridad:   
![imagen](https://user-images.githubusercontent.com/76178268/158872974-4f230c9b-05ab-4a16-bcd5-2cca9d754107.png)

El celular debería estar conectado a la VPN:   
![imagen](https://user-images.githubusercontent.com/76178268/158873016-0524f35d-f5ef-41d7-af5d-65fc963f243d.png)

## Tshark

Instalaremos Tshark para capturar el tráfico de red del celular.

```
sudo apt install tshark
```

## Captura de paquetes de red

1. En el celular con LineageOS desinstalar  y deshabilitar todas las apps no necesarias. Esto nos permitirá tener el menor ruido en la captura de tráfico.
2. Instalar la app que se quiere analizar.
3. En el servidor Ubuntu inicializar Tshark:

```
sudo tshark -i enp0s3 -w /tmp/nombre.pcap
```

La interfaz de escucha es la misma que la de nuestra ip local.

4. Conectar el celular a la VPN a través de OpenVPN.
5. Explorar la app.

# Transferencia del archivo nombre.pcap a nuestro huesped para analizar en Wireshark

Mover el archivo pcap a la carpeta /home del usuario en el servidor Ubuntu:

```
sudo mv /tmp/nombre.pcap /~
```

Darle los permisos necesarios para poderla copiar:

```
sudo chmod 777 nombre.pcap
```

En la terminal de nuestro equipo huesped:

``` 
scp usuario@192.168.x.x:nombre.pcap /home/usuario/Descargas
```

Abrirlo el archivo con Wireshark y analizar tráfico.

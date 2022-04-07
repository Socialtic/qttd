# Análisis de aplicaciones

## Captura de paquetes de red

1. En el celular (preferentemente con  LineageOS) desinstalar  y deshabilitar todas las aplicaciones no necesarias. Esto nos permitirá tener el menor ruido en la captura de tráfico.
2. Instalar la aplicaciones que se quiere analizar.
3. En el servidor Ubuntu inicializar Tshark:

```
sudo tshark -i enp0s3 -w /tmp/nombre.pcap
```

La interfaz de escucha es la misma que la de nuestra IP local.

4. Conectar el celular a la VPN a través de OpenVPN.
5. Explorar la aplicación.

## Transferencia del archivo nombre.pcap a nuestro huesped para analizar en Wireshark

Mover el archivo pcap a la carpeta /home del usuario en el servidor Ubuntu:

```
sudo mv /tmp/nombre.pcap ~
```

Darle los permisos necesarios para poderla copiar:

```
sudo chmod 776 nombre.pcap
```

En la terminal de nuestro equipo huesped:

``` 
scp usuario@192.168.x.x:nombre.pcap /home/usuario/Descargas
```

Abrirlo el archivo con Wireshark y analizar el tráfico.

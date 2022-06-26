# Análisis de aplicaciones

En esta sección mostraremos cómo capturar los paquetes de red desde una máquina virtual a la cual le instalaremos el servidor VPN, para posteriormente analizarlos desde la máquina huésped. Una máquina virtual es correr jaja

## Captura de paquetes de red

1. En el celular (preferentemente con una ROM como LineageOS) desinstalar y deshabilitar todas las aplicaciones no necesarias pues esto nos permitirá tener menos "ruido" en la captura de tráfico
2. Instalar las aplicaciones que se quiere analizar
3. En la máquina virtual inicializar `tshark` en la interfaz correspondiente
   ```bash
   sudo tshark -i enp0s3 -w /tmp/nombre.pcap
   ```
   La interfaz de escucha es la misma que la de nuestra IP local
4. Conectar el celular a la VPN a través de OpenVPN
5. Explorar la aplicación para generar tráfico

## Transferencia del archivo PCAP al huésped

Mover el archivo `.pcap` a la carpeta `$HOME` del usuario en el servidor VPN:

```bash
sudo mv /tmp/nombre.pcap $HOME
```

Cambiar el dueño del archivo y grupo

```bash
sudo chown user:user nombre.pcap
```

Transferir el archivo a nuestro equipo huésped. Podemos iniciar un servidor web con Python en la máquina virtual.

```bash
python3 -m http.server 8000
```

En un navegador desde la computadora huésped visitar la dirección IP local del servidor en el puerto 8000 y descargar el archivo, opcionalmente podemos ejecutar el comando desde la máquina huésped:

```bash
curl -O 192.168.X.X:8000/nombre.pcap
```

Abrir el archivo PCAP con `wireshark` en la máquina huésped y analizar el tráfico.

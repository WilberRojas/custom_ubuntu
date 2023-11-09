1. Descargar e instalar controladores de GPU (Nvidia): </br>
   https://www.nvidia.es/Download/index.aspx </br>
   Si no funciona, usar los siguientes comandos: </br>
   1.1. revisa los driver disponibles
   ```
   ubuntu-drivers devices
   ```
   output:
	```
	== /sys/devices/pci0000:00/0000:00:01.0/0000:01:00.0 ==
	modalias : pci:v000010DEd00002504sv00001458sd00004074bc03sc00i00
	vendor   : NVIDIA Corporation
	driver   : nvidia-driver-525-open - distro non-free
	driver   : nvidia-driver-535-server - distro non-free
	driver   : nvidia-driver-470-server - distro non-free
	driver   : nvidia-driver-525 - distro non-free
	driver   : nvidia-driver-525-server - distro non-free
	driver   : nvidia-driver-535-open - distro non-free
	driver   : nvidia-driver-535-server-open - distro non-free recommended
	driver   : nvidia-driver-535 - distro non-free
	driver   : nvidia-driver-470 - distro non-free
	driver   : xserver-xorg-video-nouveau - distro free builtin
	
	```
 	1.2. Instala el recomendado sin `-open` o `-server-open` </br>
	Ejemplo de instalacion:
	```
	sudo apt install nvidia-driver-535
	```
 	1.3. reinicia la computadora y verifica
	```
	nvidia-smi
	```
	Deberias obtener un output similar a este:
	```
	#EJEMPLO OUTPUT:
	
	Mon Jul 18 18:29:48 2022       
	+-----------------------------------------------------------------------------+
	| NVIDIA-SMI 510.73.05    Driver Version: 510.73.05    CUDA Version: 11.6     |
	|-------------------------------+----------------------+----------------------+
	| GPU  Name        Persistence-M| Bus-Id        Disp.A | Volatile Uncorr. ECC |
	| Fan  Temp  Perf  Pwr:Usage/Cap|         Memory-Usage | GPU-Util  Compute M. |
	|                               |                      |               MIG M. |
	|===============================+======================+======================|
	|   0  NVIDIA GeForce ...  Off  | 00000000:01:00.0 Off |                  N/A |
	| N/A   49C    P5    N/A /  N/A |    303MiB /  4096MiB |      0%      Default |
	|                               |                      |                  N/A |
	+-------------------------------+----------------------+----------------------+
									       
	+-----------------------------------------------------------------------------+
	| Processes:                                                                  |
	|  GPU   GI   CI        PID   Type   Process name                  GPU Memory |
	|        ID   ID                                                   Usage      |
	|=============================================================================|
	|    0   N/A  N/A      1562      G   /usr/lib/xorg/Xorg                198MiB |
	|    0   N/A  N/A      1897      G   /usr/bin/gnome-shell               34MiB |
	|    0   N/A  N/A      2579      G   ...383402268078645775,131072       24MiB |
	|    0   N/A  N/A     30532      G   ...RendererForSitePerProcess       39MiB |
	+-----------------------------------------------------------------------------+
	```
 	En caso de no funcionar intenta con las otras opciones disponibles para la misma version, en este caso `nvidia-driver-535-open` o `nvidia-driver-535-server-open`
	(recuerda que es necesario reiniciar despues de instalar un driver de nvidia)

3. Instalar Extensiones:
   
    2.1. Instalar Tweaks-Tool:  </br>
    ```
    sudo apt install gnome-tweak-tool
    ```
    2.2. Instalar Chrome:
    https://www.google.com/chrome/?platform=linux  </br>
    ```
    sudo apt install ./archivo.deb
    ```

    2.3 Instalar extensiones:
    https://extensions.gnome.org/ 

    - sugerencias: 
    https://docs.google.com/document/d/1OatrImjzqC34vFCxAh1d91v3k7T6lgrbNcu9vAUhVNY/edit?usp=sharing 

4. Personalizar Tema, Iconos, Mouse:
https://www.gnome-look.org/ 

    - Sugerencias:
    https://docs.google.com/document/d/1jHSbX7f9ohRvsQoLJVE-JSkblVVF5LtkmxlFTRrrJjM/edit?usp=sharing 

## Instalar Programas
1. Terminal:
    - Añadir repositorio*
    - Actualizar la terminal </br>
      ```
      sudo apt-get update
      ```

    - instalar: </br>
      ```
      sudo snap install <programa>
      ```
        OR </br>
      ```
      sudo apt-get install <programa>
      ```
2. .RUN

    - Hacer ejecutable: 
      Desde propiedades o `chmod +x archivo.run`
    - Instalamos:
      ```
      sudo ./archivo.run
      ```
3. .DEB

    - Instalar: </br>
      ```
      sudo apt install ./archivo.deb
      ```
4. .APPIMAGE (es portable)

    - Hacer ejecutable
    - Correr: </br>
      ```
      ./archivo.appimage
      ```
    - Crear un comando (opcional):
      * Verificar que el comando no exista
      * Mover el programa a la carpeta de comandos </br>
      	```
        sudo mv archivo.appimage /usr/bin/<comando>
       	```
	


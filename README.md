1. Instalar controladores de GPU (Nvidia):
https://www.nvidia.es/Download/index.aspx 

2. Instalar Extensiones:
2.1. Instalar Tweaks-Tool:  </br>
sudo apt install gnome-tweak-tool

    2.2. Instalar Chrome:
    https://www.google.com/chrome/?platform=linux  </br>
    sudo apt install ./archivo.deb

    2.3 Instalar extensiones:
    https://extensions.gnome.org/ 

    - sugerencias: 
    https://docs.google.com/document/d/1OatrImjzqC34vFCxAh1d91v3k7T6lgrbNcu9vAUhVNY/edit?usp=sharing 

3. Personalizar Tema, Iconos, Mouse:
https://www.gnome-look.org/ 

    - Sugerencias:
    https://docs.google.com/document/d/1jHSbX7f9ohRvsQoLJVE-JSkblVVF5LtkmxlFTRrrJjM/edit?usp=sharing 

----------------------Instalar Programas------------------------------
1. Terminal:
    - Añadir repositorio*
    - Actualizar la terminal </br>
      sudo apt-get update

    - instalar: </br>
      sudo snap install <programa> </br>
        OR </br>
      sudo apt-get install <programa>

2. .RUN

    - Hacer ejecutable: 
      Desde propiedades o chmod +x archivo.run
    - Instalamos:
      sudo ./archivo.run

3. .DEB

    - Instalar: </br>
      sudo apt install ./archivo.deb

4. .APPIMAGE (es portable)

    - Hacer ejecutable
    - Correr: </br>
      ./archivo.appimage

    - Crear un comando (opcional):
      * Verificar que el comando no exista
      * Mover el programa a la carpeta de comandos </br>
        sudo mv archivo.appimage /usr/bin/<comando>
	


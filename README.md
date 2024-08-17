# Instalacion de Máquina virtual Kali Linux

Para la creacion de la VM se decidio utilizar VirtualBox.

## Pasos:
1. Navegar a la página oficial de kali, donde se mostrarán dos opciones para seleccionar la plataforma de Kali deseada. En este caso se elige la opción “Virtual Machines”.
2. En la opción 64-bits, se selecciona “VirtualBox” para descargar una imagen completa de Kali para VirtualBox. La descarga comenzará enseguida.
3. Se descomprime el archivo zip descargado.
4. Si ya se cuenta con el GUI de VirtualBox:

    a. Abres la aplicación.

    b. En el menú de arriba, seleccionas la opción “Nueva”, navega hasta la dirección del archivo descomprimido y seleccionas el archivo “.vbox”. La máquina virtual se creará automáticamente.
5. Si no, instala la aplicación y sigue los pasos indicados en el punto 4.

**Url kali.org**: [https://www.kali.org/get-kali/#kali-platforms]

# Instalación de proxy de interceptación
Se decidió usar ZAP.
## Pasos:
1. Ingresar al sitio de descargas oficial de ZAP.
2. Selecciona el instalador que más te convenga.
3. El ejecutable se empezará a descargar automáticamente.
4. Abre el archivo ejecutable y sigue los pasos hasta finalizar la instalación.

**Url ZAP**: [https://www.zaproxy.org/download/]

# Instalación de docker en la VM
**url**: [https://www.kali.org/docs/containers/installing-docker-on-kali/]
1. Ejecutar sudo apt update
2. Ejecutar el comando ‘sudo apt install -y docker.io’ para instalar docker.
3. Ejecutar el comando ‘sudo systemctl enable docker --now’ para poder comenzar a utilizar la aplicación.
4. Ejecutando ‘ sudo usermod -aG docker $USER’ puedes darle permisos de administrador a tu usuario para no tener que utilizar el comando ‘sudo’ en cada ejecución.

# Ejecución de contenedor con OWASP Juice Shop
Primero hay que descargar la imagen del contenedor de Juice Shop para poder crear una instancia y navegar a través de la página web localmente.

## Pasos:
1. Con el comando ‘docker pull bkimminich/juice-shop’ se descarga la imagen mas actualizada.
2. Con el comando ‘docker run -d -p 127.0.0.1:3000:3000 bkimminich/juice-shop’ se corre el contendor en localhost, en el puerto 3000.
3. Navegando a http://localhost:3000 podrás visualizar la página de Juice Shop.

### Prueba de visualizacion

>[!VIDEO](./record.mp4)
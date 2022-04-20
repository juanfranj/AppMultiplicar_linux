# AppMultiplicar
Aplicacion para que mi niña repase las tablas de multiplicar.

Repositorio para deploy de la aplicación en linux con buildozer.

Pasos buildozer:
[Video youtube](https://www.youtube.com/watch?v=s3rCRFuuL9E&list=PLiPg9RMFb0x0S3GdXo5RorF8T5FSjldGO&index=1&t=1294s)

1.- Instalar WSL: - https://docs.microsoft.com/en-us/wind...
2.- Instalación Python y buildozer:
$ sudo apt update
$ sudo apt-get install git
$ sudo apt-get install python3.6
$ sudo apt-get install python3-setuptools
$ sudo apt install -y git zip unzip openjdk-8-jdk python3-pip autoconf libtool pkg-config zlib1g-dev libncurses5-dev libncursesw5-dev libtinfo5 cmake libffi-dev
$ sudo apt-get install cython
$ pip3 install --user --upgrade cython virtualenv
$ cd "home/user" (ir a un directorio donde clonaremos el repositorio)
$ git clone https://github.com/kivy/buildozer.git
$ cd buildozer
$ sudo python3 setup.py install
$ cd "app" (mover directorio de la app)
$ buildozer init
## Transmitir teléfono
Libreria ADB(transmitir dispositivo): 
https://www.xda-developers.com/instal...
(Comandos)
Windows: dentro del directorio que descargamos
.\adb kill-server
.\adb -a -P 5037 nodaemon server
Linux: (WSL 2)
$ sudo apt-get install android-tools-adb android-tools-fastboot
$ export ADB_SERVER_SOCKET=tcp:192.168.20.31:5037 (remplazar con tu IP)
$ adb devices  (para ver dispositivos conectados)

## En el directorio de la app
$ buildozer android debug deploy run logcat

* **Autor:**

    * **Juanfran**
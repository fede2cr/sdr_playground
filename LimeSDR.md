# Usando una LimeSDR

La LimeSDR es una nueva pero popular tarjeta con mucho poder para analisis de protocolos por la capacidad de leer y transmitir en dos canalis de forma simultánea a frecuencias de varios GHz donde los SDRs baratos no pueden llegar.

Sin embargo por ser tan reciente la cantidad de aplicaciones que son compatibles con la LimeSDR son limitadas

## Instalación de software
TODO: mover a ansible y a snaps

```bash
#LimeSDR
sudo add-apt-repository -y ppa:myriadrf/drivers
sudo apt-get update
sudo apt-get install limesuite limesuite-udev limesuite-images
sudo apt-get install soapysdr soapysdr-module-lms7


# Universal Radio Hacker
sudo apt-get install python3-numpy python3-psutil python3-zmq python3-pyqt5 g++ libpython3-dev python3-pip gnuradio
git clone https://github.com/jopohl/urh.git
cd urh
git checkout limesdr
sudo python3 setup.py install


```

## Universal Radio Hacker

La herramienta ideal para escuchar y hacerse pasar por teclados inalámbricos con pésima encripción, ha sido parchada recientemente para incluir soporte para LimeSDR. 

https://github.com/jopohl/urh

Se está desarrollando un Snap para poder instalar de forma sencilla la herramienta y dependencias requeridas.

https://github.com/fede2cr/snapcraft-sandbox/tree/master/limesdr-urh

Para instalar el paquete, debe ejecutar estos comando en un Ubuntu 16.04 (vesión con Unity)
```bash
sudo apt dist-upgrade
sudo apt install screen snapd snapcraft vim git
git clone https://github.com/fede2cr/snapcraft-sandbox.git
cd snapcraft-sandbox/limesdr-urh
snapcraft
sudo snap install limesdr-urh_1.6.2.2_amd64.snap --dangerous
limesdr-urh.urh
```

## QSpecrtumAnalyzer

Muy sencilla para analizar una porción grande del espectro para tener una idea de donde están sucediendo cosas interesantes en un gran espacio.

Funciona teniendo instalado Soapy_Power, definiendo en los parámetros, con su número de serie:

```
driver=lime, serial=XXXXXXXXXXXXXXXX, label=LimeSDR-USB [USB 2.0] XXXXXXXXXXXXX
```

## GQRX

El software con el que recomiendo comenzar con un RTL-SDR, al menos a mi todavía no me funciona aunque ya algunos usuarios han tenido éxito. Me encuentro probando la versión de git a ver si funciona.

https://discourse.myriadrf.org/t/limesuitegui-and-gqrx-some-observations-and-some-questions/855/8

## LimeSuite

El software que viene con la tarjeta. No es nada práctico... úselo solo para saber si la instalación quedó bien y si la tarjeta está funcionando correctamente.

# Usando una LimeSDR

La LimeSDR es una nueva pero popular tarjeta con mucho poder para analisis de protocolos por la capacidad de leer y transmitir en dos canalis de forma simultánea a frecuencias de varios GHz donde los SDRs baratos no pueden llegar.

Sin embargo por ser tan reciente la cantidad de aplicaciones que son compatibles con la LimeSDR son limitadas

## Universal Radio Hacker

La herramienta ideal para escuchar y hacerse pasar por teclados inalámbricos con pésima encripción, todavía no tiene soporte para LimeSDR aunque si, un branch y pull request del autor de la herramienta, para este fin. Traté de hacer que el branch me funcionara y aunque ya aparece en el menú, todavía no logro que funcione sin importar la frecuencia o configuración que le defina. Ya escribí para solicitar información al respecto.

https://github.com/jopohl/urh/pull/228

## QSpecrtumAnalyzer

Muy sencilla para analizar una porción grande del espectro para tener una idea de donde están sucediendo cosas interesantes en un gran espacio.

Funciona teniendo instalado Soapy_Power, definiendo en los parámetros, con su número de serie:

```
driver=lime, serial=XXXXXXXXXXXXXXXX, label=LimeSDR-USB [USB 2.0] XXXXXXXXXXXXX
```

## GQRX

El software con el que recomiendo comenzar con un RTL-SDR, al menos a mi todavía no me funciona aunque ya algunos usuarios han tenido éxito. Me encuentro probando la versión de git a ver si funciona.

https://discourse.myriadrf.org/t/limesuitegui-and-gqrx-some-observations-and-some-questions/855/8

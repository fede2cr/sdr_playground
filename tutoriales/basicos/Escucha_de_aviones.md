# Dump1090

En este ejercicio vas a poder escuchar el sistema de anuncio de aeronaves conocido como [ADS-B](https://en.wikipedia.org/wiki/Automatic_dependent_surveillance_%E2%80%93_broadcast), donde vamos a recibir de forma separada de cada aeronave información que puede incluir el código de vuelo, altitud, velocidad y hasta coordinadas geográficas, lo que permiten conocer:

- Aeropuerto de salida y llegada
- Hora de salida y llegada
- Modelo de aeronave
- Fotografías de la aeronave
- Vuelos anteriores

Con ayuda de la aplicación Dump1090 podemos capturar la información de anuncio y utilizar un mapa para graficar la ruta de vuelo de los aviones así como realizar monitoreo a largo plazo de espacio aéreo.

*Nota: Si se busca en un sitio como Github.com existen múltiples versiones del Software Dump1090. Algunas son versiones obsoletas y otras funcionan excelente pero complican el observar la información en el mapa.*

## Instalación

Para simplificar la instalación vamos a utilizar una Raspberry Pi, y cargarle la distribución llamada PiAware la cual utiliza un servicio de rastreo de aviones llamado Flightaware, y presenta una interface web muy limpia y clara para el seguimiento de altitud, con trazo de línea de ruta, etc.

### Materiales

- Una Raspberry Pi (versión 2 o 3, puede ser Zero)
- Un radio definido por software [RTL-SDR básico](https://www.amazon.com/NooElec-NESDR-Mini-Compatible-Packages/dp/B009U7WZCA) o para mejores resultados una tarjeta de [Flightaware](https://www.amazon.com/FlightAware-Stick-Receiver-Built-Filter/dp/B01M7REJJW) con una [antena para 1090Mhz](https://www.amazon.com/1090Mhz-Antenna-Connector-2-5dbi-Adapter/dp/B013S8B234)

### Pasos

1. Descargue la imagen de PiAware en la sección "Install PiAware on your SD card" de la página de [PiAware](https://flightaware.com/adsb/piaware/build)
2. Cargue la imagen de PiAware a una microSD para Raspberry Pi
3. Conecte puerto de HDMI, el radio definido por software, cable de red y arranque la Pi
4. Luego de que arranque, observe la consola de HDMI para encontrar el IP de la Pi
5. Conéctese vía Web al IP de la Pi y observe las aeronaves
6. De forma opcional puede configurar la cuenta de Flightaware para recibir atribución sobre las contribuciones de observaciones de aeronaves


## Alternativa

Si no desea dedicar una Raspberry Pi, sino solamente hacer una demostración rápida de las capacidades de ADS-B, una alternativa de software es [AirplaneJS](https://www.npmjs.com/package/airplanejs) el cual se basa en NodeJS y crea su propio servidor web.

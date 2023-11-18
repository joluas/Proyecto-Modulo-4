# Proyecto-Modulo-4

Con esta API puedes consultar toda la informacion proporcianada por el [Servicio Sismologico Nacional de la UNAM](http://www2.ssn.unam.mx:8080/catalogo/).

Los datos fueron descargados, limpiados y subidos a MongoDB desde donde la API puede hacer consultas.

A continuacion, puedes consultar todos los posibles EndPoints y parametros que pueden ser usados en esta API:

### Main URL
- Request URL: (Aqui va ir un URL)
- Request method: GET
- Request functionality: Este EndPoint te permite saber si puedes alcanzar la API de manera correcta.

### Sismos URL
- Request URL: (Aqui va ir un URL)/sismos
- Request method: GET
- Request functionality: Este EndPoint te permite conocer los detalles que contiene cada sismo en la base de datos.

### Estados URL
- Request URL: (Aqui va ir un URL)/sismos/estados
- Request method: GET
- Request functionality: Este EndPoint te permite conocer los valores que puedes usar en la API de busqueda para buscar sismos por estado.

### Busqueda URL
- Request URL: (Aqui va ir un URL)/sismos/busqueda
- Request method: GET
- Request functionality: Este EndPoint es el que te permite hacer una busqueda de sismos de acuerdo a los parametros ingresados.

#### Parametros
|Key|Value|Details|
|-------------|-------------|-----|
|state|string| Para usar correctamente el filtro de estado debes consultar el EndPoint Estados URL. Debes usar los valores proporcionado en dicha API para poder hacer busqueda de sismos por estado.|
|date|date (YYYY-MM-DD)| Los sismos dentro de la base de datos abarcan desde el 1990-01-01 hasta 2023-11-11|
|magnitude|float| La escala de Richter va desde 0 hasta 10. El sismo de mayor magnitud registrado en la base de datos es de 8.2. El sismo de menor magnitud registrado es de 0.3|

### Fun URL
- Request URL: (Aqui va ir un URL)/sismos/fun
- Request method: GET
- Request functionality: Just a little easter egg :).

# Proyecto-Modulo-4

Con esta API puedes consultar toda la informacion proporcianada por el [Servicio Sismologico Nacional de la UNAM](http://www2.ssn.unam.mx:8080/catalogo/).

Los datos fueron descargados, limpiados y subidos a MongoDB desde donde la API puede hacer consultas.

A continuacion, puedes consultar todos los posibles EndPoints y parametros que pueden ser usados en esta API:

### Main URL
- Request URL: `https://joluas.pythonanywhere.com/`
- Request method: GET
- Request functionality: Este EndPoint te permite saber si puedes alcanzar la API de manera correcta.

### Sismos URL
- Request URL: `https://joluas.pythonanywhere.com/sismos`
- Request method: GET
- Request functionality: Este EndPoint te permite conocer los detalles que contiene cada sismo en la base de datos.

### Estados URL
- Request URL: `https://joluas.pythonanywhere.com/sismos/estados`
- Request method: GET
- Request functionality: Este EndPoint te permite conocer los valores que puedes usar en la API de busqueda para buscar sismos por estado.

### Busqueda URL
- Request URL: `https://joluas.pythonanywhere.com/sismos/busqueda`
- Request method: GET
- Request functionality: Este EndPoint es el que te permite hacer una busqueda de sismos de acuerdo a los parametros ingresados.

#### Parametros
|Key|Value|Details|
|-------------|-------------|-----|
|state|string| Para usar correctamente el filtro de estado debes consultar el EndPoint Estados URL. Debes usar los valores proporcionado en dicha API para poder hacer busqueda de sismos por estado.|
|date|date (YYYY-MM-DD)| Los sismos dentro de la base de datos abarcan desde el 1990-01-01 hasta 2023-11-11|
|magnitude|float| La escala de Richter va desde 0 hasta 10. El sismo de mayor magnitud registrado en la base de datos es de 8.2. El sismo de menor magnitud registrado es de 0.3|

#### Response example
```
{
    "1.- total results": 1,
    "2.- data": [
        {
            "Estatus": "revisado",
            "Fecha": "Fri, 03 Jun 1932 04:36:52 GMT",
            "Fecha UTC": "Fri, 03 Jun 1932 10:36:52 GMT",
            "Latitud": 19.57,
            "Longitud": -104.42,
            "Magnitud": 8.2,
            "Profundidad": "33.0",
            "Referencia de localizacion": "4 km al SURESTE de CASIMIRO CASTILLO, JAL",
            "URL": "https://www.google.com/maps/search/?api=1&query=19.57,-104.42"
        }
    ]
}
```

### Fun URL
- Request URL: `https://joluas.pythonanywhere.com/sismos/fun`
- Request method: GET
- Request functionality: Just a little easter egg :).

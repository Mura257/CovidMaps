# CovidMaps
App interactiva que usa servidores, contenedores, y servidores en la NUBE AWS, que indicara cuales son los lugares con mas riesgo de contraer coronavirus, en medellin, esta le preguntara informacion al usuario, su nombre, edad, ubicacion y si tiene coronavirus, sospecha que lo tiene, o o no lo tiene, dependiendo si este sospecha o no que lo tiene, se aumentara el riesgo en la zona, si este lo tiene, el riesgo aumenta significativamente, si sospecha, este aumenta levemente y si no tiene, este no aumentara, todos estos procesos estan explicandos a continucacion


# Explicacion del diseño de la aplicacion


# DockerFile
Lo primero que tenemos en cuenta sera el dockerfile, este tendra todos los archivos, listos para ser usados en cualquier otro pc, estos archivos seran ubicados en un servidor ubuntu, y estos  archivos estaran escritos en python y usara la libreria flask, apache, y una configuracion DNS

# registro.html
Al ingresar a la app, el usuario sera saludado por este archivo, este tendra algo simple, una interfaz grafica de usuario, donde este se podra registrar, ingresar sus datos, y decir si ha tenido o tiene algun familiar que tiene coronavirus, y la ubicacion donde lo tiene, estos datos seran mandado a una BD de MYSQL

# principal.py
Aqui es donde el usuario sera redirigido despues de haber ingresado sus datos, este archivo esta encargado de "conectar" todo entre si, la base de datos, el grafico html, y el registro, despues de estar en este archivo, el usuario pasara al grafico html donde puede ver si es seguro salir o no.

# grafico.html
En el grafico html, se planea usar una implementacion de algun mapa interactivo, donde se pueda localizar los casos de coronavirus cerca de su casa, usando la base de datos mysql, y llegar a la conclusion que si es seguro salir o no a la calle

# Basededatosmysql
Este archivo, tendra toda la informacion de los usuarios que se registren en la app, su nombre, una contraseña, correo y si tiene covid-19 o no, y con esto poner a esta persona en el grafico.html

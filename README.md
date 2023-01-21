# Ejercicio de Odoo:

Creamos el docker-compose con todos los datos necesarios, con el puerto 5432, que es por defecto de postgres. Una vez introducidos los datos, lo ejecutamos con docker-compose up. Una vez realizado eso tendriamos la base de datos de postgres levantada, debido a que los datos de la base de datos desaparecen cada vez que se cierra el container, creamos un volumen para guardar los datos en el:

![volumes](https://user-images.githubusercontent.com/91197989/213867571-d49393f7-a98a-478d-bcde-de1fe6189b18.png)


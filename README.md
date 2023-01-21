# Ejercicio de Odoo:

Creamos el docker-compose con todos los datos necesarios, con el puerto 5432, que es por defecto de postgres. Una vez introducidos los datos, lo ejecutamos con docker-compose up. Una vez realizado eso tendriamos la base de datos de postgres levantada, debido a que los datos de la base de datos desaparecen cada vez que se cierra el container, creamos un volumen para guardar los datos en el:

![volumes](https://user-images.githubusercontent.com/91197989/213867571-d49393f7-a98a-478d-bcde-de1fe6189b18.png)

Una vez relaizado el volumen, descargamos la imagen de odoo con el siguiente código:

![odoo](https://user-images.githubusercontent.com/91197989/213867648-13a7cf78-7999-493c-8e1c-662bfdb2bef5.png)

Y el docker-compose final temdría que ser algo similar a esto:

![odoo1](https://user-images.githubusercontent.com/91197989/213867694-06820673-959a-45c8-be15-f7967d85d49e.png)

# Ejercicio de Odoo:

Creamos el docker-compose con todos los datos necesarios, con el puerto 5432, que es por defecto de postgres. Una vez introducidos los datos, lo ejecutamos con docker-compose up. Una vez realizado eso tendriamos la base de datos de postgres levantada, debido a que los datos de la base de datos desaparecen cada vez que se cierra el container, creamos un volumen para guardar los datos en el:

![volumes](https://user-images.githubusercontent.com/91197989/213867571-d49393f7-a98a-478d-bcde-de1fe6189b18.png)

Una vez realizado el volumen, descargamos la imagen de odoo con el siguiente código:

![odoo](https://user-images.githubusercontent.com/91197989/213867648-13a7cf78-7999-493c-8e1c-662bfdb2bef5.png)

Y el docker-compose final temdría que ser algo similar a esto:

Para la base de datos usamos la imagen de postgres13 y con usuario y contraseña odoo.
Usamos el puerto 5432, puede que este puerto este ocupado asi que haremos lo siguiente: 

Buscamos que proceso está ocupando este puerto disponemos de comandos que nos listan los procesos activos: ps -> para listar los procesos activos con -aux -> lista todos los procesos del dispositivo

netstat -> lista los procesos activos y conectados al pc -pt -> tdp -put -> tdp/udp -putan -> servidores y establecidos | grep * * -> para filtrar

Tras haber encontrado el proceso usando por ejemplo nestat -putan | grep 5432 utilizaremos el comando service para parar el proceso que deseemos. Para ello podemos comenzar buscando el nombre del proceso para asegurarnos usando sudo service ( y en este caso) pos (ya que buscamos postgresql) tras esto nos mostrará los procesos que comiencen por lo indicado. Una vez verificado usaremos sudo service postgresql stop para pararlo y liberar el puerto que este usando en este caso el 5432 por lo cual ahora podremos volver a lanzar nuestro docker-compose y tenerlo en dicho puerto.

Usamos la imagen de odoo 14.0
Creamos un container llamado dam22odoo
Usamos los puertos 8069:8069

![odoo1](https://user-images.githubusercontent.com/91197989/213867694-06820673-959a-45c8-be15-f7967d85d49e.png)

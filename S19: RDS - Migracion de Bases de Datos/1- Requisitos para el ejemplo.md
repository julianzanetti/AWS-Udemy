# Preparar el entorno para el ejemplo de Replica.
- ### Crear una BD en RDS (en nuestro ejemplo vamos a utilizar un mariadb).
- ### Vamos a utilizar una instancia EC2 con acceso publico como servidor para nuestra BD.
> [!NOTE]
> Si tenemos que realizar una migracion desde un On-premise, recordar que DMS (Database Migration Service) tiene que tener acceso a nuestra Base de Datos.
> Es decir, nuestra BD tiene que estar accesible para DMS.

- ### Instalar mariadb en nuestro servidor.
```
sudo amazon-linux-extras install mariadb
```

- ### Iniciar mariadb.
```
systemctl start mariadb
systemctl enable mariadb
systemctl status mariadb
```

- ### Conectarnos a nuestra instancia EC2 y pasamos nuestros archivos sql.
> [!NOTE]
> Los archivos .sql quedaron alojados dentro de la Carpeta S19: RDS - Migracion de Base de Datos.
> Los dos archivos son archivos de ejemplos.

- ### Ingresamos a nuestro mariadb y creamos nuestra BD.
```
sudo mysql -u root -p
create database curso_aws;
```

- ### Cargamos los datos a nuestra nueva BD.
```
use curso_aws;
source /home/empleados.sql
source /home/productos.sql
```

- ### Verificamos que se haya cargado correctamente.
```
show tables;
select * from empleados;
```

- ### Creamos un usuario de migracion y le damos todos los permisos en la BD.
```
mysql -u root -p
create user 'dms'@'%' identified by 'migracion';
grant all on curso_aws.* to 'dms'@'%'
```

- ### Probamos ingresando remotamente a la BD con el usuario creado.
```
mysql -u dms -p -h ip_publica_servidorec2
```

# Preparar el entorno para el ejemplo de Replica.
- ### Crear una BD en RDS (en nuestro ejemplo vamos a utilizar un mariadb).
![image](https://github.com/user-attachments/assets/7d6a8ab8-5064-436f-893e-b4bc3683f598)

- ### Vamos a utilizar una instancia EC2 con acceso publico como servidor para nuestra BD.
![image](https://github.com/user-attachments/assets/18db2a5d-f47a-43f1-8de2-6144dac93612)

> [!NOTE]
> Si tenemos que realizar una migracion desde un On-premise, recordar que DMS (Database Migration Service) tiene que tener acceso a nuestra Base de Datos.
> Es decir, nuestra BD tiene que estar accesible para DMS.

- ### Instalar mariadb en nuestro servidor.
```
sudo amazon-linux-extras install mariadb
```
```
yum install mariadb-server # Para RHEL/CentOS/AlmaLinux
```

- ### Iniciar mariadb.
```
systemctl start mariadb
systemctl enable mariadb
systemctl status mariadb
```
![image](https://github.com/user-attachments/assets/437243cd-1012-46b6-8a79-baa93bece0e5)


- ### Conectarnos a nuestra instancia EC2 y pasamos nuestros archivos sql.
![image](https://github.com/user-attachments/assets/7cf508ab-6db1-42fd-9191-b62458631a8a)

> [!NOTE]
> Los archivos .sql quedaron alojados dentro de la Carpeta S19: RDS - Migracion de Base de Datos.
> Los dos archivos son archivos de ejemplos.

- ### Ingresamos a nuestro mariadb y creamos nuestra BD.
```
sudo mysql -u root -p
create database curso_aws;
```
![image](https://github.com/user-attachments/assets/400b9550-a321-4865-b1ac-fe108da3896e)

- ### Cargamos los datos a nuestra nueva BD.
```
use curso_aws;
source /home/empleados.sql
source /home/productos.sql
```
![image](https://github.com/user-attachments/assets/9fc5aeb4-453e-4c55-a71b-ca8b03ae6628)

- ### Verificamos que se haya cargado correctamente.
```
show tables;
select * from empleados;
```
![image](https://github.com/user-attachments/assets/3d969a68-14e9-49ec-a7bf-da9af7b7864d)
![image](https://github.com/user-attachments/assets/3afe9f26-36f7-40b7-bcab-9e7eec10dc27)

- ### Creamos un usuario de migracion y le damos todos los permisos en la BD.
```
mysql -u root -p
create user 'dms'@'%' identified by 'migracion';
grant all on curso_aws. * to 'dms'@'%';
```
![image](https://github.com/user-attachments/assets/f6f8b657-b89a-490b-8260-39f6e4135562)

- ### Probamos ingresando remotamente a la BD con el usuario creado.
```
mysql -u dms -p -h ip_publica_servidorec2
```
![image](https://github.com/user-attachments/assets/49f58110-0a33-432f-b41a-145968daecc4)

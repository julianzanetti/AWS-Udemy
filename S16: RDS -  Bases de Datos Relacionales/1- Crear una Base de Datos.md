# Crear una Base de Datos.
## Nos dirigimos a esta ruta.
![image](https://github.com/user-attachments/assets/5b913394-89f0-4730-9cd0-070711fa5ebd)

## Seleccionamos la BD que queremos instalar y su version.
![image](https://github.com/user-attachments/assets/57c53909-031a-4aec-b6c7-1b8dd44967a2)
![image](https://github.com/user-attachments/assets/0bb343cf-cd05-4206-a437-550123c9407b)

## Elegimos una plantilla.
![image](https://github.com/user-attachments/assets/1972e496-1dc7-4e7a-9742-981c7be5ddf6)

## Ingresamos el nombre de la BD, el usuario maestro y su contraseña.
![image](https://github.com/user-attachments/assets/bbcdb578-2e8f-4368-b392-1deb88d74086)

## Seleccionamos la maquina donde se alojara nuestra BD.
![image](https://github.com/user-attachments/assets/4f5311e8-b02c-45d7-9782-90141a3e2a3d)

## Configuramos el almacenamiento.
![image](https://github.com/user-attachments/assets/7d9a1932-61ea-41ca-a159-711627ea2b61)
> [!TIP]
> Importante habilitar la autoescalada. Esto nos permite (si nos quedamos sin espacio) subir hasta un tope MAX que asignemos.

## Seleccionamos nuestra VPC.
![image](https://github.com/user-attachments/assets/bc3da88d-db2b-4eb3-9eb8-471ce92c0267)

## Completamos los siguientes datos segun necesidad.
![image](https://github.com/user-attachments/assets/7b443d3a-907b-4984-8bff-0a75c11dd01e)
> [!IMPORTANT]
> Crear un Grupo de Seguridad con el puerto de nuestra BD habilitado. No usar el default que permite todas las conexiones.

## Configuracion Adicional.
### Podemos asignar un nombre a una BD inicial.
![image](https://github.com/user-attachments/assets/6f96051c-316a-43f5-a3b5-01e286e072ba)

### Habilitar backups de nuestra BD.
![image](https://github.com/user-attachments/assets/8b63ddc7-3af0-470b-b63c-29bf501a4c30)

### Elegimos si actualice o no automaticamente nuestra BD.
![image](https://github.com/user-attachments/assets/b5ea8fe5-8b79-48c1-b9f4-0c3bdc8fab88)

### Podemos habilitar la proteccion contra eliminacion.
![image](https://github.com/user-attachments/assets/7b5f3be5-39ef-4a85-a868-1bcd5c4ace1d)

## BD creada, probamos conectarnos.
![image](https://github.com/user-attachments/assets/2827480d-28bc-4d11-837e-ea2b4446079a)
```
mysql -u root -p -h 
```
![image](https://github.com/user-attachments/assets/49adec18-fc9c-4c2a-98a7-a89416375979)

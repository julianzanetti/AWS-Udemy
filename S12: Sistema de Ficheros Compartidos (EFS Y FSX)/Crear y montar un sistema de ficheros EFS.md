# Crear y montar un file system EFS a una instancia.
## Vamos a crear nuestro sistema de fichero (Recordar abrir el puerto de NFS).
### Nos dirigimos aca.
![image](https://github.com/user-attachments/assets/5cc7079c-e6dc-4041-85fd-f84f350d0a8a)

### Le damos crear un sistema de archivos.
![image](https://github.com/user-attachments/assets/bac1bdfe-8b57-4f83-89d1-f03617c72475)
![image](https://github.com/user-attachments/assets/5fd0a15a-f112-474c-863a-2d9991a2e836)

## Montarlo en una instancia.
### Ingresamos dentro de nuestro sistema de archivos y le damos asociar.
![image](https://github.com/user-attachments/assets/6e29a6e1-89ad-48cc-b26e-608370f0f464)

### Elegimos como lo queremos asociar.
![image](https://github.com/user-attachments/assets/1b598032-089a-4376-86e4-ebf7bb49e3dc)

### Dentro del servidor creamos una carpeta y asociamos el efs a dicha carpeta.
```
mkdir nombre-carpeta
sudo mount -t nfs4 -o nfsvers=4.1,rsize=1048576,wsize=1048576,hard,timeo=600,retrans=2,noresvport 10.0.132.229:/ nombre-carpeta
```
![image](https://github.com/user-attachments/assets/fdb22038-71d4-483a-a67e-f80e2f509229)

## Creamos otra instancia y lo montamos ahi tambien
### Primero vamos a crear algunos archivos en el servidor1.
![image](https://github.com/user-attachments/assets/71b817fd-b641-4f2d-84bf-4767f107071b)

### Ahora lo asociamos al servidor2.
![image](https://github.com/user-attachments/assets/87fb8a2f-3920-4fcf-9a83-121066eed178)

## Visualizamos en los dos servidores los archivos creados.
### Servidor2.
![image](https://github.com/user-attachments/assets/8218d834-9732-4557-b70c-333831409b2d)

### Servidor1.
![image](https://github.com/user-attachments/assets/ddb8e45c-78d3-4fa6-bd16-5235eb6a01e5)

## Crear un archivo en el servidor1 y visualizar en el servidor2.
![image](https://github.com/user-attachments/assets/eaf964e0-9e25-4e32-b699-bc420aad2d9f)
![image](https://github.com/user-attachments/assets/cb2f3dfd-37f4-451f-8eba-a17b37f52c02)

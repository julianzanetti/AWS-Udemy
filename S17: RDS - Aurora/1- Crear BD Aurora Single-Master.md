# Crear BD Aurora Single-Master
## Nos dirigimos a la siguiente ruta y elegimos entre MySQL y Postgresql.
![image](https://github.com/user-attachments/assets/94b87b0b-3e3d-4e08-b91a-63abb49e3eec)

## Configuramos el nombre del cluster y las credenciales de la misma.
![image](https://github.com/user-attachments/assets/c5aff137-1988-4b15-9a1b-0a73eb1490ec)

## Seleccionamos la instancia.
![image](https://github.com/user-attachments/assets/68f5587c-cd05-4903-a35e-2e531944353a)

## Elegimos si crear una replica en otra AZ.
![image](https://github.com/user-attachments/assets/1daf70db-4df1-4f13-acb4-af90ffdeff19)

## Configurar la conectividad.
![image](https://github.com/user-attachments/assets/48a95648-cd0a-41ea-95b9-2724d8d4d0ea)

## Completamos la configuracion adicional.
![image](https://github.com/user-attachments/assets/5bfde9fd-fc86-4497-a96e-c4368e9361d5)

> [!NOTE]
> Failover priority: Seleccionamos que replica actue como master cuando la primaria se caiga.

## BD creada con su respectiva replica en solo lectura.
![image](https://github.com/user-attachments/assets/9d2349a9-efb7-4878-9d4a-ae06cc155fd5)

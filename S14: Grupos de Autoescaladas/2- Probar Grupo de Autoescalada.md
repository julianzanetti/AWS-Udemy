# Probar Grupo de Autoescalada.
## Reduccion del Autoscaling Groups.
![image](https://github.com/user-attachments/assets/54aa2ee6-f64a-4584-8dea-d03cd86a4395)

Como configuramos que la politca de escalado automaticamo para que agregue o elimine en caso de que alcance el 10% de uso de CPU.

![image](https://github.com/user-attachments/assets/cd68edde-5d94-47ef-b98e-c222ad814d6c)
Como en este caso no estamos usando casi nada de CPU, entonces nos bajo a la min deseada.

## Instalamos el paquete stress para alcanzar el 10% de uso de CPU.
### Para las AMIS de amazon:
```
amazon-linux-extras install epel
yum install stress
```
## Utilizamos el paquete instalado y verificamos la actividad.
```
stress -c 10
```
![image](https://github.com/user-attachments/assets/3d099fd2-bd05-4cd5-af25-24a2a44f0844)
![image](https://github.com/user-attachments/assets/c36a671c-7b93-413e-9a7a-4be36b11bdbb)

### Si lo aumentos a 20, vemos que escala al total que hemos definido.
![image](https://github.com/user-attachments/assets/623f0fce-2f96-413f-8920-6dbc1a11e155)
![image](https://github.com/user-attachments/assets/4418d398-31c4-42b5-a059-8861fea41af4)
![image](https://github.com/user-attachments/assets/4ce159d4-2d63-4ba5-8cb9-63dd18061dc3)

### Cuando bajamos el uso de la CPU, empieza a bajar la cant. de instancias nuevamente.

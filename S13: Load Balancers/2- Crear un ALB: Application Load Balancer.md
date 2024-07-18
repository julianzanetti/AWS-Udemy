# Crear un ALB: Application Load Balancer y probarlo.
## Nos dirigimos a esta ruta.
![image](https://github.com/user-attachments/assets/e9886a48-fbb4-4343-8f12-0d6e91c5be80)

## Seleccionamos el tipo de LB que vamos a utilizar (en este caso el ALB).
![image](https://github.com/user-attachments/assets/7564cb40-5cbf-4428-934b-946cab509581)

## Completamos el nombre, si esta expuesto a internet o es interno y el tipo de direccion IP.
![image](https://github.com/user-attachments/assets/f2d1cc96-e0b2-4354-9f35-8b7248cbc4db)

## Seleccionamos nuestra VPC y mapeamos nuestras subredes.
![image](https://github.com/user-attachments/assets/37e4ca90-9f5d-4d3a-9b50-41958012b3de)

## Seleccionamos nuestro grupo de seguridad.
![image](https://github.com/user-attachments/assets/14a9a0f1-a34c-4b8f-8307-3863f26a9a99)

## Configuramos el listener para que todo lo que se escucha en el puerto 80 vaya a nuestro Target Group.
![image](https://github.com/user-attachments/assets/f0292af9-8d04-4214-a627-005a975a1abf)

## Verificamos que todo este correctamente configurado.
![image](https://github.com/user-attachments/assets/08640fc2-94e7-4b8b-9b9d-71ed313588ab)
![image](https://github.com/user-attachments/assets/e107bbd8-a87f-42db-bbd5-3d59839f5908)
![image](https://github.com/user-attachments/assets/a6c03ccd-2a39-4d15-ab50-7407096d0438)

## Verificamos en el Target Group.
![image](https://github.com/user-attachments/assets/5ae8c285-f0ad-47a4-8251-e4229673073b)

## Probamos el ALB creado ingresando con el DNS del balanceador.
### Ingreso n°1:
![image](https://github.com/user-attachments/assets/d8354fc0-3c4c-4437-aefe-976240640a23)

### Ingreso n°2:
![image](https://github.com/user-attachments/assets/5b50cdd1-b306-43f4-aa20-036b1dda114a)

### Ingreso n°3:
![image](https://github.com/user-attachments/assets/3cadf9d3-74b2-4921-a7f9-0757c8c3a63f)

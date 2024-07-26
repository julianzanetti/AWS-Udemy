# Politica de Escalado Simple y STEP.
### Nos dirigimos a crear una nueva Politica de Escalado.
![image](https://github.com/user-attachments/assets/9995a537-e8a1-4814-8393-9318b5b29f4e)

Estas politicas van de la mano con una alarma de CloudWatch. Cuando esta alarma se activa, tiene que realizar la accion que determinamos.

## Politica de Escalado Simple.
Esta nos permite Añadir, Remover o Establecer entre un nro de instancias sin la necesidad de una alarma de CloudWacht.
![image](https://github.com/user-attachments/assets/000bd317-3271-488e-8382-5176b2bfa77d)

### Ej: Si se dispara una alarma, que elimine una instancia.
![image](https://github.com/user-attachments/assets/ee7ad9d5-cc1f-4785-b3b1-98a97b743693)

### Actualmente tenemos 2, si ejecutamos nuestra nueva politica:
![image](https://github.com/user-attachments/assets/a62f879f-06b0-46f7-b535-49c693b58774)
![image](https://github.com/user-attachments/assets/4d6166d0-ff90-4f5f-85a1-9fd5cbb048ff)

### Vemos como disminuye la cantidad de instancias.
![image](https://github.com/user-attachments/assets/bd19d512-78a4-4ba8-82cd-7a9c564251f2)
![image](https://github.com/user-attachments/assets/dc7e458d-cce2-4424-bb80-0653d1f32ff5)

## Politica de Escalado por Pasos.
### - Si o si tiene que accionarse por una alarma de Cloudwacht.
### - Cuando seleccionamos una alarma, esta nos permite elegir los pasos a seguir. Ej: Subir el nro de maquinas cuando ingresen mas de 3 usuarios simultaneos.
![image](https://github.com/user-attachments/assets/305d319e-5a59-49dd-9b0f-51c714353ed4)

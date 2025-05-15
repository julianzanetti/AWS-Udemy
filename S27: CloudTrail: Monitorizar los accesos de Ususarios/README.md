# CloudTrail: Monitorización accesos de usuarios.
- Es una herramienta de monitorización de la actividad de las cuentas de AWS. Se captura toda la actividad de AWS y se puede guardar en la consola de CloudTrail, a un bucket S3 o en CloudWatch Log.
- Podemos activar alarmas en eventos.
- Se puede encontrar información en la consola o en otros servicios como Amazon Athena (queries sobre ficheros de log con lenguaje light SQL).
- Otro servicio es **`CloudTrail lake`** donde almacenamos los datos como Data store y podemos hacer consultas SQL.
- Por defecto, se capturan todos los datos de administración gratuitos, reteniendolos por 90 días.
- **`Cloud Trail Lake`** nos permite guardar la información más tiempo, pero es caro.

## Dashboard:
![image](https://github.com/user-attachments/assets/fd803bb2-74f5-4334-9d49-3bed6d799df0)

## Definiciones:
- **`Trails (Registro de Seguimientos)`**: Es un contenedor donde guardamos los eventos con los que trabajar. Cuando creamos uno podemos configurar:
![image](https://github.com/user-attachments/assets/40c9b434-0f41-41f8-8cce-c4caa6d0bdd0)
![image](https://github.com/user-attachments/assets/7c5fa1c9-4829-40b9-b864-f2cb0eadeb3e)
![image](https://github.com/user-attachments/assets/e5294054-d71e-496f-b734-f15b0efa115c)
**`Bucket creado por el Trails`**: En el bucket crea un esqueleto de carpetas para guardar eventos.
![image](https://github.com/user-attachments/assets/e40beebb-71d0-4c27-aced-458768231883)
En **`CloudTrail-Digest`** se guardan ficheros de metadatos. En **`CloudTrail`** estarán lo eventos que se guardan con un esqueleto de region y fecha en json comprimidos.

- **`Consola Cloud Trail Lake`**: Guarda los eventos en un formato que permite las SQL queries
![image](https://github.com/user-attachments/assets/fe8e89b1-19bf-4ac2-93fd-08c7b9302c36)
**`Ejemplo Consulta SQL`**:
![image](https://github.com/user-attachments/assets/fee09aec-44e4-4271-b7ac-89ccd3eb191f)

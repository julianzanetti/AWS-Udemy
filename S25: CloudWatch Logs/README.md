# CloudWatch Logs.
- CloudWatch Logs es el entorno que almacena archivos de logs.

## Conceptos.
- **`Log Events:`** Son los eventos registrados en logs. Es un registro de alguina actividad que ha guardado una aplicación o el recurso que se está monitorizando. Contiene dos propiedades:
  - **`Timestamp:`** Cuando se produjo el evento.
  - **`Mensaje del evento sin procesar:`** Son otras herramientas las que procesan el mensaje.
- **`Log Stream:`** Es una secuencia de log events que comparten el mismo origen. Representar la secuencia de eventos procedente de una aplicación o recurso.
- **`Log Groups:`** Un grupo de Log Stream que comparten las mismas características. Cada Log Stream pertenece a un Log Group.
- **`Metric Files:`** Permiten estraer dobservaciones y datos.
- **`Logs Insights :`** Para efectuar búsquedas dentro de los grupos de logs. Se pueden buscar patrones, filtrar filas, información concreta, etc.

## Ejemplo1 - Generar Logs desde RDS:
-  Cuando creamos una BBDD, por una parte, desde monitoring podemos configurar eventos que se envían a CloudWatch:
![image](https://github.com/user-attachments/assets/d774f723-d884-446d-a739-a3d4ad6de579)

Además, en opciones avanzadas podemos indicar los logs concretos que queremos que se envíen.
![image](https://github.com/user-attachments/assets/9d73197d-f4fe-423b-8f2f-9793402889f8)

Los logs de error siempre se mandan, pero los otros tres (Audit, General y Slow Query) no se mandarán por si solos. Debemos configurar los parámetros con un parameter group que lo indique:

![image](https://github.com/user-attachments/assets/d944ee71-b287-411c-931a-7045f444bdb9)

Ahora, en la BBDD creada con el paremeter group configurado y los logs activado, podemos ver los logs. Y en CloudWatch, en el grupo de logs “RDSOSMetrics” aparecerán los logs de SO de esta BBDD (CPU, RAM, etc) por tener activada la monitorización detallada.

## Ejemplo2 - Capturar el tráfico de las VPC con VPC Flow Logs.
![image](https://github.com/user-attachments/assets/9db30bae-7cf4-44f5-8e19-118b99cb25a2)
- Para crear un Flow log debemos estar en las VPCs y tiene una pestaña Flow Logs.

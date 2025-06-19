# AWS Lambda
- Nos permite trabajar en entornos `serverless`.
- Ejecuta el código en una infraestructura informática de alta disponibilidad y realiza todas las tareas de administración de los recursos informáticos, incluido el mantenimiento del servidor y del sistema operativo, el aprovisionamiento de capacidad y el escalado automático, así como la monitorización del código y las funciones de registro.
- Se puede ejecutar código para prácticamente cualquier tipo de aplicación o servicio de backend y esta basado en eventos.
-  El código se ejecuta basado en respuesta a eventos de otros servicios de Amazon como por ejemplo S3, DinamoDB, peticiones HTTP, etc. Solo tenemos que poner nuestro código dentro del servicio Lambda, configurar el trigger y esperar a que se reciban los eventos que disparan el trigger.
-  [Documentacion Oficial Lambda - AWS](https://docs.aws.amazon.com/es_es/lambda/latest/dg/welcome.html?icmpid=docs_lambda_help).

## Algunos Conceptos:
- `Handler`: Es el fichero main, el que se ejecutará el primero cuando se reciba el evento. Desde este fichero se iniciarán el resto.
- `Evento`: Son los parámetros de la función, los que se tratarán.
- Las funciones Lambda pueden ser invocadas por eventos externos o por internos como SNS, S3, CloudFormation, etc. En el segundo caso los eventos son específicos, los parámetros quelanzan según el servicio se tendrán que consultar en la documentación.
- `Contexto`: Es el entorno donde se lanza la versión Lambda. Por ejemplo, tenemos en la documentación el contexto de cuando se trabaja con Python: [Ejemplo Contexto con python](https://docs.aws.amazon.com/lambda/latest/dg/python-context.html)

## AWS Step Functions.
- Es un servicio de orquestación que le permite conectar sus funciones de Lambda en flujos de trabajo sin servidor, denominados máquinas de estado.
- Cree flujos de trabajo de larga duración para la automatización de TI y los casos de uso de aprobación humana, o cree flujos de trabajo de gran volumen y corta duración para el procesamiento e ingestión de datos en streaming.
![image](https://github.com/user-attachments/assets/ae9f85f5-d820-4662-817f-18a6aee2a0f3)

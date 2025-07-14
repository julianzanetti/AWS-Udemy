# SQS – Servicio de mensajes de Amazon
- `Amazon SQS` proporciona colas para la mensajería de alto rendimiento entre sistemas. Puede utilizar las colas para desacoplar procesos pesados y para almacenar en búferes y por lotes el trabajo. Amazon SQS almacena los mensajes hasta que los microservicios y las aplicaciones sin servidor los procesan.

## Diferencia SNS vs SQS
-  La diferencia es que `SNS` es un sistema distribuido publicar-suscribirse. Los mensajes son empujado a los suscriptores cuando los editores los envíen a SNS.
-  En cambio, `SQS` esta distribuido hacer cola sistema. Los mensajes no son empujado a los receptores. Los receptores tienen que sondear o tirar mensajes a SQS (pull).
  - Varios receptores no pueden recibir mensajes al mismo tiempo. Cualquier receptor puede recibir un mensaje, procesarlo y eliminarlo. Otros receptores no reciben el mismo mensaje más tarde.
  - El sondeo introduce inherentemente cierta latencia en la entrega de mensajes en SQS, a diferencia de SNS, donde los mensajes se envían inmediatamente a los suscriptores
  - SNS admite varios puntos finales como correo electrónico, SMS, punto final HTTP y SQS. Si desea que un número y tipo de suscriptores desconocidos reciban mensajes, necesita SNS.

- SQS es un sistema distribuido, un receptor recibe el mensaje, lo procesa y lo elimina. No puede haber más recpetores.
<img width="720" height="330" alt="image" src="https://github.com/user-attachments/assets/2751efc2-7dd2-4a2f-942e-326cda07e176" />

## Tipos de Cola de Mensajes.
- Estandar:
  - Tienen un nivel de procesamiento ilimitada.
  - Los mensajes se entregan al menos una vez.
  - El orden de entrega puede ser distinto al del envío. La aplicación tiene que ser consciente de este hecho y tratar el mensaje de forma coherente
- FIFO – First In First Out:
  - Se admiten hasta 300 mensajes por segundo y agrupando se pueden conseguir hasta 3000 mensajes por segundo.
  - Los mensajes solo se mandan una vez hasta que se procesan y eliminan. No se introducen duplicados.
  - El orden de entrega es igual al del envío.

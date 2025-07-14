# SQS – Servicio de mensajes de Amazon
- `Amazon SQS` proporciona colas para la mensajería de alto rendimiento entre sistemas. Puede utilizar las colas para desacoplar procesos pesados y para almacenar en búferes y por lotes el trabajo. Amazon SQS almacena los mensajes hasta que los microservicios y las aplicaciones sin servidor los procesan.

## Diferencia SNS vs SQS
-  La diferencia es que `SNS` es un sistema distribuido publicar-suscribirse. Los mensajes son empujado a los suscriptores cuando los editores los envíen a SNS.
-  En cambio, `SQS` esta distribuido hacer cola sistema. Los mensajes no son empujado a los receptores. Los receptores tienen que sondear o tirar mensajes a SQS (pull).
  - Varios receptores no pueden recibir mensajes al mismo tiempo. Cualquier receptor puede recibir un mensaje, procesarlo y eliminarlo. Otros receptores no reciben el mismo mensaje más tarde.
  -  El sondeo introduce inherentemente cierta latencia en la entrega de mensajes en SQS, a diferencia de SNS, donde los mensajes se envían inmediatamente a los suscriptores

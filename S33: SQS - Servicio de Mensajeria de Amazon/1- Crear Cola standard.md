# Cola standard
Cuando creamos una cola standard podemos configurar:
- `Visibility Timeout`:  El tiempo que está invisible mientras se procesa el mensaje.
- `Periodo de retención del mensaje`:  Los mensajes que no se reclaman se eliminan después de este tiempo.
- `Delevery delay`: Cuanto espera un mensaje que llega a la cola en estar disponible.
- `Capacidad máxima del mensaje`.
- `Receive message wait time`: Determina si hacemos short o long polling (Sondeo corto o largo).
> [!NOTE]
> Con `Short polling` se recoge un conjunto de servidores y se devuelve, no mira todos los servidores. Utiliza un proceso aleatorio, con lo que puede quedarse alguno fuera. Si ponemos más de 0 segundos será Long Polling se preguntará a todos los servidores de manera que se devolverán todos los mensajes.

<img width="735" height="313" alt="image" src="https://github.com/user-attachments/assets/9604084b-774d-4a7f-a81a-343fd50c7ff1" />

En este ejemplo de short polling vemos que no recoge todos los mensajes, le falta E que lo recogerá en un segundo polling. Short polling es razonable con menos de 1000 mensajes.
- `La politica de Acceso`: En basico nos da las opciones de quien puede enviar mensajes y quien puede enviarlos.

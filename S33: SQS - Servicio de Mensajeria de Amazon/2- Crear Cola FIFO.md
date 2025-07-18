# Cola FIFO
 Cuando creamos una cola FIFO además de las propiedades standard podemos configurar:
 - `Content-based deduplication`: En cada mensaje le dará un hash para controlar que no hayan repetidos. Si no utilizamos esta opción, el productor del mensaje tendrá que dar a cada mensaje un messageDeduplicationId para poder identificar inequivocamente cada mensaje.
 - `Enable high throughput FIFO`: Si lo habilitamos el scope y el limite será por grupo de mensajes.
   - `Deduplication scope`
     - Por cola
     - Por Grupo de mensajes
   - `FIFO throughput limit`
     - Por cola
     - Por ID de grupo de mensajes.
La deduplicación tiene un tiempo de 5 minutos de control. Pasado ese tiempo deja de controlar si el 
mensaje ha llegado. A día de hoy este rango no se puede cambiar.

## Colas de Mensajes Muertos
<img width="1180" height="392" alt="image" src="https://github.com/user-attachments/assets/ba5070a0-effe-4ddc-948e-eda9f1886a00" />
Las DLQ nos permiten reconducir los mensajes a la cola fuente para volver a procesar. Para esto necesitamos una cola del mismo tipo que la cola a la que queramos ponerle DLQ (Standard con standar y FIFO con FIFO). Una vez creada, nos vamos a Dead-letter queue de la cola origen y editamos para activar el Dead-letter queue. Indicamos la cola de mensajes incorrecto (La cola creada) y el número de mensajes que queremos que provoque que vaya a la cola de incorrectos. Ahora, en la cola de mensajes incorrectos, marcamos DLQ redrive indicando que los mande a la cola original. Podríamos indicar otra cola de mensajes.

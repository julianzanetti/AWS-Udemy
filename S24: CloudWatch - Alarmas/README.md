# CloudWatch Alarmas
![image](https://github.com/user-attachments/assets/813944db-7ea2-4c19-80ec-1f9b7bf21bde)
- **`Todas las alarmas`** tenemos todas las alarmas configuradas.
- **`En modo alarma`** tenemos las alarmas que se han disparado.
- Los símbolos, de izquierda a derecha:
  - **`Alarmas activas`**
  - **`Alarmas ok`**
  - **`Alarmas sin datos suficientes:`** Suele ser provocado por estar recien creada o no tiene suficientes DataPoint para saber si está correcta.

## Crear una Alarma.
- Se crea en 4 pasos:
![image](https://github.com/user-attachments/assets/d9240762-8212-4be1-b3ef-5ebe50c927e0)

- Como ejemplo vamos a crear una alarma de CPU que se conecte al SNS y envíe un correo.
- Primero seleccionamos la métrica, luego decidimos las condiciones con un valor estático o con una función de anomalía (un rango de
comportamiento).
![image](https://github.com/user-attachments/assets/0eaf254d-f725-44dd-b645-7a2231cb5fe7)

- Una vez tenemos la métrica y las condiciones ya podemos escoger la acción entre:
- **`Enviar una notificación:`** Se puede enviar una notificación si se dispara una alarma, si la alarma se quita y paso ok, o si no hay datos suficientes. Se selecciona o se crea el topic. Se puede enviar más de una notificación, se pueden añadir.
- **`Una acción de auto escalada:`** Se selecciona un grupo de autoescalada y se especifica la tarea.
- **`Una acción EC2:`** – Podemos hacer un recover (las instancias pequeñas no lo soportan), parar la instancia, Terminarla o reiniciarla.
- **`Una acción System Manager.`**
![image](https://github.com/user-attachments/assets/026f15bb-c9f4-4f80-b210-cc46a56ab793)

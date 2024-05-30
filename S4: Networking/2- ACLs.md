# Introduccion a los ACL.
Los ACL son una herramienta de seguridad que permite controlar el tráfico entrante y saliente a nivel de subred en tu VPC. Ej:
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/e47e1c17-e7ee-4240-86ad-4cf90da8bb71)
Vemos que en el ejemplo anterior se permite la entrada de todo trafico desde cualquier sitio.

![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/38eb0b05-1f0b-4f4d-b3ce-f17eab6d81d8)
Lo mismo en las reglas de salida.

### Editar mi regla de entrada/salida
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/3fd4379f-5c79-4cb1-8003-0c9a14ad23c2)
En el ejemplo estamos permitiendo las regla de entrada al puerto 22 desde cualquier sitio, el numero de regla 10 es para que se cumple primero esta y despues la 100.

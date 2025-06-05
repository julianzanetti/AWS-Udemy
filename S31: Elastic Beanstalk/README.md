# Compute – Elastic Beanstalk
- Permite **`implementar y administrar aplicaciones`** dentro de la nube de AWS sin tener que preocuparse por la infraestructura que las ejecuta.
- Se pueden desplegar en python, en node, en java, en go, en .NET, en php y ruby… sin indicarle si necesita un balanceador de carga, un grupo de seguridad… A través de un asistente creará un entorno apropiado a la aplicación.
![image](https://github.com/user-attachments/assets/8d21515d-3962-4129-8c59-e9b059b7be89)

- Reduce la complejidad de la administración sin restringir la libertad de elección ni el control.
- Solo tiene que **`cargar la aplicación`** y Beanstalk gestionará de manera automática los detalles de aprovisionamiento de capacidad, balanceo de carga, escalado y monitorización de estado de la aplicación.
![image](https://github.com/user-attachments/assets/59fe6091-3b52-420f-8020-7bb4021d3c66)

- Los componentes son accesibles para poder modificarlos.
- Cuando se implementa la aplicación se crea la versión de la plataforma compatible seleccionada y aprovisiona uno o varios recursos de AWS, como instancias EC2.
- Una vez finalizada la instalacion, Beanstalk crea un entorno de enviroment.
![image](https://github.com/user-attachments/assets/8ba49196-77c8-46f5-ace3-f02d25b05aaf)
- Crea un bucket, un grupo de seguridad, un target group, crea una instancia en EC2, un grupo de autoescalado, alarmas CloudWatch y un balanceador de carga.
- Si ingresamos al dominio proporcionado vemos nuestra aplicacion web de ejemplo.
![image](https://github.com/user-attachments/assets/28b10f1e-f66d-40c6-9731-1855813a2a28)

## Politica de despliegues.
- **`All at once`**: Es el despliegue más rápido porque actualiza en todas las instancias al mismo tiempo, pero durante ese tiempo la aplicación estará parada.
- **`Rolling`**: No habrá indisponibilidad. Irá actualizando una instancia trás otra. Se puede indicar porcentaje de máquinas en cada actualización o el número de máquinas que actualiza a la vez
- **`Rolling with additional batch`**: Tarda un poco más en acabar la actualización que el anterior, porque creará nueva instancias para poder atender las peticiones de los usuarios. Se podrá mantener el ancho de banda.
- **`Immutable`**: No actualiza instancias, crea nuevas y vuelve a desplegar la aplicación. Es el que más tarda.}
![image](https://github.com/user-attachments/assets/6c828a7c-f079-4400-bebb-9e9b9a049c9d)

## Restaurar entorno
- Cuando finalizamos un entorno podemos volver a restaurar el mismo en la ultima version como se dejo.
![image](https://github.com/user-attachments/assets/3f29817f-b7a9-455b-bcfb-f109b17d49ed)

# Replicas Autoscaling.
## Nos dirigimos a esta opcion.
![image](https://github.com/user-attachments/assets/ca8abc85-1be7-4091-b344-ead53c738f27)

## Ingresamos un nombre para la politica y seleccionamos una politica de metrica.
![image](https://github.com/user-attachments/assets/fc0de592-61e8-4c93-9b69-da3e05759790)

> [!NOTE]
> En este ejemplo usamos la politica de cantidad de conexiones, con un target de 2.

## Indicamos la capacidad del cluster.
![image](https://github.com/user-attachments/assets/a8d8c7c2-f93f-480b-a400-ead38d18fe6d)

> [!NOTE]
> En este ejemplo pusimos como min una replica y como max 15.

## Ejemplo de funcionamiento.
### Simulamos varias conexiones al endpoint del mysql.
![image](https://github.com/user-attachments/assets/4d75d0e1-9803-412c-8729-43b030dc6b14)

### Se visualiza dentro de los logs las advertencias y aumento de replicas.
![image](https://github.com/user-attachments/assets/72b8d399-4e7c-4b2b-b7da-ba882f83d360)

### Visualizamos la cantidad de replicas hechas por el autoescalado.
![image](https://github.com/user-attachments/assets/dc8d4de1-185a-48b7-99ca-ea79a3c9c3ab)

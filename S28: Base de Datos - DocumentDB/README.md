# Bases de Datos: DocumentDB
-  Una versión de MongoDB en AWS. Está orientada a Cloud. Cualquier dato en MongoDB es fácil reapuntarla a DocumentDB.
## Conceptos Basicos:
- NOSQL (NotOnlySQL) es una evolución del sistema clásico de BBDD relacionales cuya principal característica es que no se requiere una definición inicial de las estructuras sobre las que se almacenarán los datos. 
- Evolución del modelo entidad-relación para el soporte de estructuras variables en el tiempo.
- MongoDB es una BBDD NOSQL orientada a documento.
- Desarrollada por 10gen (Ahora llamados MongoDB)

## Características
- Flexibilidad de los Modelos
- Alto rendimiento, alta disponibilidad
- Escalabilidad
- Permite tener documentos dentro de documentos
- Podemos definir arrays dentro de documentos.
- El modelo de documentos se basa en el estándar JSON/BSON (BSON es una serialización binaria de JSON). Características de BSON

### Comparación SQL vs MongoDB
![image](https://github.com/user-attachments/assets/d2e054f6-a5d0-4929-9487-dcfd66f126d5)

### Ejemplo de un documento con vista JSON
![image](https://github.com/user-attachments/assets/d3d9e12c-c459-4809-8a8c-824f07dfa487)
- Este documento sería una fila, se podría subir a una collection, que sería una tabla.

## Arquitectura.
- Un cluster consta de 0 a 16 instancias y un volumen de almacenamiento de cluster que gestiona los datos de esas instancias.
- Los datos del clúster se almacenan en el volumen del clúster con copias en tres zonas de disponibilidad diferentes.
![image](https://github.com/user-attachments/assets/73f6f275-9b5d-4e29-a083-ee8a93dfc348)

- El cluster volume es el almacenamiento global. Solo escriben datos la instancia primaria. Tanto la primaria como las réplicas leen datos.

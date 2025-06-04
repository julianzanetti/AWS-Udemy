# Compute – Lightsail
- Dentro de Compute AWS ofrece distintos servicos:
  - `AWS app Runner`: Permite desplegar desde código fuente o desde un contenedor en un entorno escalable, orientado a contenedores.
  - `Batch`: Procesa cargas de trabajo en modo batch dentro la nube
  - `EC2: Elastic Compute`: Máquinas virtuales
  - `EC2 Image Builder`: Constructor de AMIs
  - `Elastic Beanstalk`: Implementar y administrar aplicaciones dentro de la nube de AWS sin tener que preocuparse por la infraestructura que las ejecuta.
  - `Lambda`: Permite ejecutar código en un entorno severless.
  - `Ligthsail`: Entorno destinado a usuarios con menos nivel técnico donde pueden crear instancias, contenedores, BBDD, redes, etc
  - `Outpost`: Permite ejecutar servicios de AWS en entornos on-premise.

- ### Ligthsail tiene 6 tipos de creaciones de componentes de manera rápida:
  - `Instances`:
    - Se puede seleccionar la zona y la imagen.
      ![image](https://github.com/user-attachments/assets/e4912720-b8cc-4ebb-aa43-2416b8bc64a1)
    - Blueprint son entornos preparados con aplicaciones para poderlos crear una instancia rápida con ellos
      ![image](https://github.com/user-attachments/assets/fa48c1fd-5d92-408b-8a86-f7fd0dab3a20)
    - Se puede añadir un script de lanzamiento, seleccionar el ssh keypair y habilitar los snapshots automaticos.
      ![image](https://github.com/user-attachments/assets/c7d3bd24-11fa-4520-a3e0-5eb269b27818)
    - Se escoge el plan.
      ![image](https://github.com/user-attachments/assets/d1d896dd-7887-484f-a6e7-a9bd9d9dc2dd)
  - `Containers`: Podemos crear nuestros contenedores Docker, como si fuese ECS (Elastic Containers Services) o EKS (Elastic Kubernetes Services) pero con una gestión simple.
  - `Databases`: La creación es bastante parecida a la opción “easy" de RDS. Podemos escoger entre MySQL y PostgreSQL.
  - `Networking`: Se puede crear IP estática, Balanceador de carga de HTTP y HTTPS, CDN (Content Delivery Netowrk) y Zona DNS.
  - `Storage`: Podemos crear Buckets y Discos
  - `Snapshots`

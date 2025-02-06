# Grupo de Recursos y editor de Tags.
- Una buena **`política de etiquetas`** nos puede servir para poder tener categorizados con una jerarquía los objetos desplegados. De esta manera, desde la monitorización en CloudWatch o desde el control 
de costes en Billing, tendremos facilidad para informes, para aplicar métricas, para gestión y control de multitud de aspectos. Es IMPORTANTE la decisión de una política de etiquetado en la infraestructura entre los miembros de la organización
- Con **`Resource Groups & Tag Editor`** podemos tener un control de la gestión de las etiquetas. Además, podemos creas plantillas de infraestructura con CloudFormation.
- En el **`Editor de Tags`** podemos etiquetar masivamente recursos concretos de forma que lo podamos agrupar en un grupo de recursos. Los parámetros que podemos usar para filtrar son por Regiones, por tipo de recursos y/o por etiquetas ya existentes. **`Ej:`**

![image](https://github.com/user-attachments/assets/c2e16a00-277d-4836-83f0-2c048ac84103)
![image](https://github.com/user-attachments/assets/59b979ba-e1f4-4aca-9f76-c778c04d4c6a)

- Una vez le damos a buscar recursos nos aparece un listado desde donde podemos seleccionar para etiquetar con el **key:valor** que queramos clicando en **`Manager tags`**.

- En **`crear un grupo de recursos`** podemos basarlo en Tags o en CloudFormation stack. Basados en Tags tenemos las siguiente configuración:
  - Se puede agrupar con unos criterios concretos, por ejemplo, buscando recursos directamente en un listado o añadiendo directamente las etiquetas key:valor. Hacemos una preview de los resultados de filtrado.
![image](https://github.com/user-attachments/assets/0527362f-a2f2-44e9-ad3f-bab031d667bf)
![image](https://github.com/user-attachments/assets/56967081-b36b-4bdc-b3fa-4d71ab65159b)

  - Se puede agrupar otros grupos de recursos
  - Nombre y descripción del grupo
  - Etiquetas de grupo (Opcional)

Una vez se cree se pueden ver en **`Saved Resource Groups`**
![image](https://github.com/user-attachments/assets/3651e8b7-ec0d-46bd-9f41-2ed0575fd2ce)

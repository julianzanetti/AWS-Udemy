# Versionado de Plantillas
Una vez creada nuestra plantilla, cuando entramos dentro de esta nosotros podemos ver los detalles (detalle de la instancia, almacenamiento, etiqueta, etc), sus versiones, sus etiquetas:
![image](https://github.com/julianzanetti/Aws-Udemy/assets/134458575/84bafdc8-b5ed-4e41-95cf-8e7725a8258d)

Cuando queremos modificar una plantilla, esta crearia una nueva version con la modificacion que hayamos hecho. Ej:
![image](https://github.com/julianzanetti/Aws-Udemy/assets/134458575/74640f00-335b-4021-85e0-05f720f326e6)

Como vemos en el ejemplo, la version 2 tiene un servidor un poco mas grande que es el t2.small a diferencia de la version 1 que tiene el t2.micro.

Esto nos permite crear un grupo de escalamiento o una flota de spot para cada version de plantilla por separado, tambien podemos elegir que version seria la predeterminada o directamente eliminar dicha version.
![image](https://github.com/julianzanetti/Aws-Udemy/assets/134458575/95a20c1b-f29f-4ed9-bc85-c68cb1f90b96)

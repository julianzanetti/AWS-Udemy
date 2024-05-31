# Servidor en red privada pueda salir a internet.
### El requisito seria que el servidor se encuentre en la misma VPC que el servidor con salida a internet.
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/0e596b53-d622-4b78-89f7-c4fcb65aa7cb)

### Prueba de que no tiene salida a internet.
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/bb1e96ea-b834-49cc-b3c2-ad49b69eec08)

### Primer paso seria crear una IP elastica.
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/1107839d-ed44-4ff8-9ff3-fb38dda2bf13)
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/bf6cbac4-7330-4a13-a35c-60624e8425fc)

### Creamos nuestro NAT Gateway.
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/712e05b5-3ef6-412a-b61a-60b2d96a32a9)
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/2a3e7e06-2c60-466d-8960-85b447c071e3)

Recordar asignarle la subred publica y tambien la IP elastica que creamos anteriormente.

### Habilitamos el NAT dentro de la subred privada.
Nos dirijimos a la tabla de ruta de nuestra subred privada y agregamos nuestra NAT.
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/6ee9027f-619f-42ab-ae60-5a52c00dcd31)
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/6359e4cc-1da0-4e49-8c9e-20fb188555cd)

### Nos conectamos a nuestro servidor en red privada.
Ingresamos desde el servidor con red publica, que tiene el 22 habilitado. Le pasamos la llave y nos conectamos.

![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/658a47e7-d9fc-4df6-9c72-d868c6848d75)
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/bcfb8d91-d4fc-4b2b-bd81-46f55370be98)

### Verificamos que ya tenemos salida a internet.
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/8d4b3f65-45f6-4cbb-b3d1-5484296f9247)

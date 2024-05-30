![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/b87a7e97-6794-438d-8fa3-b722ef965a76)# Subred Publica
#### Panorama general de una VPC con sus respectivas zonas y una subred publica con Internet Gatewey.
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/38f6a743-849b-4b70-8ac0-2e6f95d9c5e1)

### Creamos nuestra subred publica.
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/e69a1950-1085-4e9b-87fb-2b900839b810)

Vemos que esta subred se vincula a la misma tabla de ruta ya que estamos en la misma VPC.
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/4aec08b8-a879-4f8a-a94e-3f70c7d390b5)

### Creamos un Internet gateway en esta ruta.
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/602e8687-e26e-4070-b5fe-3b01772ba07b)
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/282510d4-7652-4d4b-99b5-f6b97ef40074)

### Asociar nuestro gateway a la VPC.
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/551cedf7-ed2a-4bfc-ab2e-b278fbfe65a0)

Seleccionamos nuestra gateway y damos en Conectar a la VPC.
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/783201fd-5793-4d31-ba03-76c0a1089ca4)

Ahora cambia el estado a attached.
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/62a24812-09a7-44ed-a750-0baa38131cb3)

### Crear nueva tabla de ruta para salir a internet.
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/76166ae7-3c82-4602-a152-603ac1275046)

Configuramos nuestra tabla de ruta.

![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/0e172272-0570-417b-8b71-82a9a5ef35f6)

### Dentro de rutas, editamos nuestra rutas y añadimos nuestra preferencia para que podamos salir a internet.
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/cbae081e-884f-4c1f-82fa-6ffff05c14e0)
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/62a86943-2297-45a3-a363-c2fabc4f9f6c)

### Asociamos nuestra tabla de ruta que configuramos recientemente.
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/1ff1c687-c151-418f-bccc-3d3c12ebc41a)

Seleccionamos nuestra tabla de ruta y guardamos cambios.
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/d65c15b9-1d90-4de4-be80-7e1d6a207263)

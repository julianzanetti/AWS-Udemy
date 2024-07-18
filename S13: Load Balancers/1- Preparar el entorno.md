# Preparar el entorno para aplicar un Load Balancer.
## Requisitos
1. Nuestra VPC tiene que contar con mas de una subred.
2. La subredes deben estar en Z.A distintas. Ej:
![image](https://github.com/user-attachments/assets/b43e6aef-48b0-484e-9365-3eecb2892e73)

3. Para nuestro ejemplo vamos a necesitar tener instalado en nuestros servidores el servicio de Apache (httpd).
![image](https://github.com/user-attachments/assets/d2f1118a-879e-4375-b60d-8fb8a3bb0d6f)
![image](https://github.com/user-attachments/assets/d88bca9d-9ac4-4f43-910c-b97c4a88e578)

4. Crear el Target Group (Grupos de Destino).

## Target Group.
### En nuestro caso vamos a trabajar con instancias.
![image](https://github.com/user-attachments/assets/2b8d8a23-127c-460c-90fe-d1f9d14ddd3c)

### Elegimos el nombre, el protocolo, Tipo de direccion IP, la VPC donde se encuentra nuestras intancias.
![image](https://github.com/user-attachments/assets/0925c579-b706-456a-9bb2-dabae17c9f56)

### Seleccionamos las intancias que van a formar parte del grupo y su respectivo puerto.
![image](https://github.com/user-attachments/assets/5247226e-3364-4c94-ac30-81a5b9c61eca)
![image](https://github.com/user-attachments/assets/f8ff9f8d-8b3f-4d27-9e20-7d87a2bfd8b3)

### Verificamos que este todo correcto.
![image](https://github.com/user-attachments/assets/d7fc74f2-df42-4f8d-9fd1-f0e66c548459)
![image](https://github.com/user-attachments/assets/ed6b1a3e-7a5f-4cd6-81b7-12723912de1e)

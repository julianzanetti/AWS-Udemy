# Creando objetos. Crear una instancia EC2.
## Primero consultamos el ID de la AMI que vamos a seleccionar.
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/c2dfc04d-81c5-4e4a-84d9-17c223a38628)
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/ff670f6f-227d-478e-b7d1-c890fe7dc141)

## Tambien seleccionamos el ID de nuestro par de claves y grupo de seguridad que vamos a utilizar.
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/99d80541-c78e-4b5a-a633-6351e66a7787)
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/5e3cac52-c546-4fc8-a36f-1849605b983b)

## Ejecutamos el siguiente comando para la creacion de la instancia EC2.
```
aws ec2 run-instances --image-id ami-0111a2997be700b15 --count 1 --instance-type t2.micro --key-name linux-capa-gratuita --security-groups ServidoresCapaGratis
```

## Verficamos la creacion de la instancia.
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/a81b33e9-3073-4830-854c-f9995e2e034e)

## Verificamos la instancia con el comando.
```
aws ec2 describe-instances
```
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/5bbd7d6b-44d5-4071-9120-5975a4a3ff43)
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/ed2584b3-ae55-4be8-b776-9625aa59fcde)

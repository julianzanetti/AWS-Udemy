# Ejemplos con AWS CLI.
## Vamos a consultar nuestras AMIs.
```
aws ec2 describe-images --owner self
```
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/614855ad-8b9b-466c-af37-1cf202b04119)

## Filtramos solamente el nombre.
```
aws ec2 describe-images --owner self --query 'Images[].Name'
```
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/c749c8fe-c8b1-4204-965f-58bfa103ec43)

## Crear un AMI con una instancia ya en ejecucion.
```
aws ec2 describe-instances --query 'Reservations[].Instances[].[InstanceId,State]'
```
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/eabf03a4-7a42-4cd1-b4e3-6d52d6b086fc)

```
aws ec2 create-image --instance-id i-0689731a86800b407 --name AMI-AWS-CLI
```
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/74ee64d1-3dfe-45d7-9a2d-3158752190e2)

## Volvemos a consultar nuestras AMIs.
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/f8a135e4-aee6-4c2a-beb9-feadf0373792)

## Vamos a eliminar esta AMI creada recientemente junto con su snapshot.
```
aws ec2 deregister-image --image-id ami-00bde2f06f8b5a8a5
```
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/2b345807-1ccf-4279-9a4d-5f25acc3d3de)

```
aws ec2 delete-snapshot --snapshot-id snap-0e25af7769b07df65
```
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/007053a0-0431-47f4-a2c3-6f6c9ffc883e)

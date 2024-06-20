# Filtros de Columnas [query].
## Mostrar la segunda subred.
```
aws ec2 describe-subnets --query 'Subnets[1]'
```
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/45804714-ebe0-4504-a6f6-4a6fe28d45da)

## Mostrar todas las zonas de dispobinilidad.
```
aws ec2 describe-subnets --query 'Subnets[].AvailabilityZone'
```
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/7d0ad38c-63c8-48c6-9289-143d1f75c4c6)

## Visualizar los Tags.
```
aws ec2 describe-subnets --query 'Subnets[].Tags'
```
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/12301429-c028-4ebf-a0b3-80ee9c6aa409)

## Mostrar solamente los primeros dos tags.
```
aws ec2 describe-subnets --query 'Subnets[0:3].Tags'
```
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/0aa35c46-a6ac-4185-aff7-dcbb887c183b)

## Mostrar los ID y las zonas de dispobinilidad.
```
aws ec2 describe-subnets --query 'Subnets[].[SubnetId,AvailabilityZone]'
```
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/f4fc1d71-e105-49b7-a678-79d0f8f43157)

## Ahora la misma consulta anterior pero con una etiqueta para distinguir que consulamos en la salida.
```
aws ec2 describe-subnets --query 'Subnets[0:2].[{"Subred ID":SubnetId},{"Zona Disponibilidad":AvailabilityZone}]'
```
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/e570221a-2483-433b-9662-0e9f615af6bb)

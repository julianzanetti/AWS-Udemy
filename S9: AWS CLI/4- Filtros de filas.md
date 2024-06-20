# Filtros de filas en las consultas (--filter).
## Describimos las subredes que tengamos.
```
aws ec2 describe-subnets
```
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/28618d8f-0ae9-4103-aaf5-4618bc646355)

## Buscamos las subredes solo por ID.
```
aws ec2 describe-subnets --subnet-ids [valor]
```
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/14bc0059-67e4-4f5b-ba7c-2046a3660c4a)

## Filtramos por zona de dispobinilidad.
```
aws ec2 describe-subnets --filters "Name=availability-zone, Values=sa-east-1b"
```
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/094a89df-ecca-4682-9a12-89a693afbeab)

## Filtramos por zona y vpc.
```
aws ec2 describe-subnets --filters "Name=availability-zone, Values=sa-east-1c" "Name=vpc-id, Values=vpc-004d2726706107c87"
```
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/6696afd8-88df-4cd6-a39a-df3bd52e60cd)

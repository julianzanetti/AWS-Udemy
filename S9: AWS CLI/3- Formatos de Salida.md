# Formatos de Salida.
## Vamos a consular nuestras vpc.
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/4f9b5939-cc74-4d0a-b5d0-ca2c2efc1c69)
```
aws ec2 describe-vpcs
```
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/6fb1792c-b696-4ff3-9f71-7fff6a2c1863)

## Formato de consulta yaml.
```
aws ec2 describe-vpcs --output yaml
```
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/e9fdee42-e9a5-481b-9598-77fe653cfd42)

## Formato de consulta texto.
```
aws ec2 describe-vpcs --output text
```
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/86c1f224-c762-40bc-8c1c-d515ed29dea6)

## Formato en modo tabla.
```
aws ec2 describe-vpcs --output table
```
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/04763872-18c8-4347-8e9b-86564aad9598)

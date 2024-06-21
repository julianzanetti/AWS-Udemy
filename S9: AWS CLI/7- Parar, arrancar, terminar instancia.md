# Parar, arrancar, terminar instancia
##Verificamos el ID de nuestra instancia.
```
aws ec2 describe-instances --query 'Reservations[].Instances[].{"Id Instancia":InstanceId}'
```
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/bb26f7fd-845a-47a3-b1ae-77d14821ce1b)

## Parar una instancia.
```
aws ec2 stop-instances --instance-ids ID
```
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/666b1e5c-c13f-425a-b172-6259bb1eb727)

## Verificamos en la web.
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/a820c15f-e410-4447-9bad-e6a0f7e29fa4)

## Arrancamos la instancia.
```
aws ec2 start-instances --instance-ids ID
```
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/bd8e4d15-3b1c-495f-a7ee-b8512b05bb46)

## Verificamos en la web.
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/57ce6626-c6bf-435e-8583-f905c5778430)

## Terminamos la instancia.
```
aws ec2 terminate-instances --instance-ids ID
```
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/e8935f1c-4de3-4d64-9b46-f186ffafae6b)

## Verificamos en la web.
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/596341fe-8f48-4521-a3a5-5d6fbdc4890c)

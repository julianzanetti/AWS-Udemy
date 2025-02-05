# Ejemplo SNS con AWS CLI.
## Listar los topic que tengamos.
```
aws sns list-topics
```
![image](https://github.com/user-attachments/assets/83e46813-36fd-4860-9abb-8a50e6997174)

## Crear un topic.
```
aws sns create-topic --name <nombre-del-topic>
```
![image](https://github.com/user-attachments/assets/f8ae92d8-8e6a-421c-8b7a-7ebd79bb4fbc)
![image](https://github.com/user-attachments/assets/c806ac70-001d-4021-9c99-4d5f2f41ef58)

## Listar las suscripciones.
```
aws sns list-subscriptions
```
![image](https://github.com/user-attachments/assets/b75219e7-e057-45ef-9136-e1c5eb692ebc)

## Crear una suscripcion de tipo email.
```
aws sns subscribe --topic-arn arn:aws:sns:sa-east-1:123456789012:mi-topic --protocol email --notification-endpoint usuario@example.com --region sa-east-1
```
![image](https://github.com/user-attachments/assets/f0305a1a-5453-4bdf-bb2b-028f1dbe03a4)
![image](https://github.com/user-attachments/assets/872ae9ab-bc6a-40d0-bf64-7b81beb91935)

## Eliminar suscripcion y topic.
- ### Suscripcion.
```
aws sns unsubscribe --subscription-arn <ARN-de-la-suscripción>
```
![image](https://github.com/user-attachments/assets/d53244d1-5247-4572-b897-014aea626c71)

- ### Topic.
```
aws sns delete-topic --topic-arn <ARN-del-topic>
```
![image](https://github.com/user-attachments/assets/63760f7a-1af7-4ec7-910e-72a53665eda8)

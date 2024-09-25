# Practicas con AWS CLI.
## Crear una base de datos RDS de tipo Mysql.
```
aws rds create-db-instance --db-instance-identifier db-20 --db-instance-class db.t3.micro --engine mysql --master-username admin --master-user-password contrasenha --allocated-storage 20
```
![image](https://github.com/user-attachments/assets/a72ca59d-585b-4aea-b241-0677a9bd1ed7)

## Comprobar que se haya creado tanto en consola como en comando.
```
aws rds describe-db-instances --query DBInstances[].DBInstanceIdentifier
```
![image](https://github.com/user-attachments/assets/7ce452e4-44f0-4162-a27b-c7c722750950)
![image](https://github.com/user-attachments/assets/7a89ff0c-a633-405e-adee-669868fb110e)

## Crear un snapshot de la base de datos.
```
aws rds create-db-snapshot --db-instance-identifier db-20 --db-snapshot-identifier snap-20
```
![image](https://github.com/user-attachments/assets/8f2f39c1-b63e-415a-89c2-cf14c5205429)

## Comprobar que se ha creado, tanto en la consola como en modo comando
```
aws rds describe-db-snapshots
```
![image](https://github.com/user-attachments/assets/887eb477-d087-4785-beca-7b6028608d89)
![image](https://github.com/user-attachments/assets/76ac7f1d-9ac2-4055-8c0d-45dd264f6549)

## Visualizar solo el nombre del snapshot
```
aws rds describe-db-snapshots --query "DBSnapshots[*].{Name:DBSnapshotIdentifier}"
```
![image](https://github.com/user-attachments/assets/90ef4f94-ac94-4b51-adea-3bd4517b7e4b)

## Borrar el snapshot
```
aws rds delete-db-snapshot --db-snapshot-identifier snap-20
```
![image](https://github.com/user-attachments/assets/cf243540-f2b3-41f1-b0f2-7c0ac48da0b7)

## Borrar la Base de datos
```
aws rds delete-db-instance --db-instance-identifier db-20 --skip-final-snapshot
```
![image](https://github.com/user-attachments/assets/0e975d99-4e66-4720-bd71-f720fcb50cc1)

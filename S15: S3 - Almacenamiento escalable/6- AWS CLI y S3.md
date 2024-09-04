# AWS CLI y S3.
## Crear un bucket S3 y listar nuestros buckets.
```
aws s3 mb s3://bucket_julian
aws s3 ls
```
![image](https://github.com/user-attachments/assets/536b580b-3375-4baf-83dc-7593d7d4cc58)
![image](https://github.com/user-attachments/assets/4545a24f-1f30-498d-b519-ca17096c5667)

## Copiar un fichero local a nuestro bucket.
```
aws s3 cp fichero.txt s3://bucket-julian
```
![image](https://github.com/user-attachments/assets/62622320-cf34-4598-9178-b6d5b8cf3314)
![image](https://github.com/user-attachments/assets/025d3d17-178f-44b7-ac8f-27b9365b5c7b)

## Borrar el fichero recien creado.
```
aws s3 rm s3://bucket-julian/fichero.txt
```
![image](https://github.com/user-attachments/assets/625f496b-cc70-49b6-ba85-51270e28a7b1)
![image](https://github.com/user-attachments/assets/b363e241-b40f-41aa-8c3a-4785fc016c2d)

## Eliminar el bucket.
```
aws s3 rb s3://bucket-julian
```
![image](https://github.com/user-attachments/assets/ff0e2473-90bc-410e-b648-68831072b853)

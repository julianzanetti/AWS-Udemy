# S3: Mandar una notificacion al crear un objeto
![image](https://github.com/user-attachments/assets/e1b1c87f-a0b2-46e4-abcd-11e57cd16694)

## Antes debemos darle los permisos necesarios a S3 en SNS.
- Nos dirigimos a nuestro topic.
![image](https://github.com/user-attachments/assets/439c0b75-1688-4a4b-9960-f0615237d171)

- Editamos la politica de acceso para que S3 pueda esrcibir.
```
{
    "Version": "2012-10-17",
    "Id": "example-ID",
    "Statement": [
        {
            "Sid": "Ejemplo SNS",
            "Effect": "Allow",
            "Principal": {
                "Service": "s3.amazonaws.com"
            },
            "Action": [
                "SNS:Publish"
            ],
            "Resource": "SNS-topic-ARN",
            "Condition": {
                "ArnLike": {
                    "aws:SourceArn": "arn:aws:s3:*:*:bucket-name"
                },
                "StringEquals": {
                    "aws:SourceAccount": "bucket-owner-account-id"
                }
            }
        }
    ]
} 
```

## Creamos la notificacion para el evento.
![image](https://github.com/user-attachments/assets/be748328-51fe-4049-a17c-590f71017fde)
![image](https://github.com/user-attachments/assets/26b58634-7984-4214-bd59-04038ccf0418)
![image](https://github.com/user-attachments/assets/888ffd85-f823-472f-ab08-d6523c6a789c)

## Probamos nuestro SNS añadiendo un ficherito.
![image](https://github.com/user-attachments/assets/aacdfb98-9d2f-4f57-a888-4baf578d65ee)

## Verificamos que haya llegado la notificacion.
![image](https://github.com/user-attachments/assets/b234cff8-75f8-424a-badf-5446eef7f273)

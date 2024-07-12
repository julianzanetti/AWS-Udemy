# Ver, crear, asociar y desasociar volumenes con AWS CLI.
## Listamos los volumenes que tengamos.
```
aws ec2 describle-volumes
```
![image](https://github.com/user-attachments/assets/9938763e-6b2f-4a69-87b4-3cccc99fa0b9)

## Mostramos solamente el ID del volumen y su instancia.
```
aws ec2 describe-volumes --query 'Volumes[].[{Volumen:VolumeId},Attachments[].{Instancia:InstanceId}]'
```
![image](https://github.com/user-attachments/assets/79952cb1-1507-4697-a3ea-c87c90adeb58)

## Creamos un volumen.
```
aws ec2 create-volume --availability-zone sa-east-1a --size 5 --volume-type gp2
aws ec2 describe-volumes --query 'Volumes[].[{Volumen:VolumeId}]
```
![image](https://github.com/user-attachments/assets/8e3716b0-ba76-4b52-a2e3-6e507969225e)
![image](https://github.com/user-attachments/assets/5c6a9686-a83a-49cb-a2c7-65235c141dd0)
![image](https://github.com/user-attachments/assets/f51c8281-20f7-4010-a974-d08385d947f3)

## Vamos a asociar el volumen creado.
```
aws ec2 describe-volumes --query 'Volumes[].[{Volumen:VolumeId},Attachments[].{Instancia:InstanceId}]' --output yaml
```
![image](https://github.com/user-attachments/assets/2a6fa97f-52c8-4427-a89b-370f3fa4a6c9)

```
aws ec2 attach-volume --volume-id vol-0a8cbf8f9d336a3ab --instance-id i-011565d14e1182b63 --device /dev/sdh
```
![image](https://github.com/user-attachments/assets/1ee31e63-a9bd-4b50-a585-a739c2e18e15)
![image](https://github.com/user-attachments/assets/bb65c5b5-91a8-4aab-9f72-769e742f8b12)
![image](https://github.com/user-attachments/assets/3f892c4b-2330-4a3e-944f-9478af2bad00)

## Desasociar el volumen de la instancia.
```
aws ec2 detach-volume --volume-id vol-0a8cbf8f9d336a3ab --instance-id i-011565d14e1182b63
```
![image](https://github.com/user-attachments/assets/26214f04-0dea-4823-9efc-745e683521ad)
![image](https://github.com/user-attachments/assets/e77ece75-6740-40a4-9a9d-ac36c4d46bc7)

## Vamos a borrar el volumen creado.
```
aws ec2 delete-volume --volume-id vol-0a8cbf8f9d336a3ab
```
![image](https://github.com/user-attachments/assets/74dccce0-7d2c-44e8-a884-3d7a4a12c58a)

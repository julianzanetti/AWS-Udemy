# Particionar, formatear y montar el volumen en una instancia.
## Verificamos exista la particion vinculada a la instancia.
```
df -h
cd /dev
ls -l sd*
```
![image](https://github.com/user-attachments/assets/850ab3b1-ba83-4967-8353-cb989c32e504)

## Vamos a particionar el disco.
```
fdisk /dev/xvdb
n
p
1
default
defualt
w
```
![image](https://github.com/user-attachments/assets/ac297b2d-ef30-484a-9771-e82fe4182811)
![image](https://github.com/user-attachments/assets/ead3539c-9f1c-42a7-b4e9-9fee057701df)

## Verificamos la nueva particion creada.
![image](https://github.com/user-attachments/assets/1a7cc9ca-15a5-4f77-b813-ccd8ea4b2b78)

## Vamos a crear el sistema de fichero con mkfs (filesystem).
```
ls -l /dev/sd*
mkfs.xfs nombre.particion
```
![image](https://github.com/user-attachments/assets/903d23a0-300f-45ed-9252-656db43a64ca)

## Ahora toca montar la nueva particion.
```
mkdir /dev/disco2
mount /dev/nombre.particion /dev/disco2
```
![image](https://github.com/user-attachments/assets/ef722c59-f1be-4d56-b69e-94c5a05891b5)

## Verificamos que se haya montado correctamente.
```
df -h
```
![image](https://github.com/user-attachments/assets/051671e8-df08-4fa6-92a8-0c46848a9b54)

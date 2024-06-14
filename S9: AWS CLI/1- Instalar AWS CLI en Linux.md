# Instalar AWS CLI
## Instalamos AWS CLI con los siguientes comandos.
```
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
unzip awscliv2.zip
sudo ./aws/install
```
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/afb707c8-08f5-4877-9c4c-3dd18904b9be)

## Para actualizar el AWS CLI.
```
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
unzip awscliv2.zip
sudo ./aws/install --bin-dir /usr/local/bin --install-dir /usr/local/aws-cli --update
```

# Instalar un Agente de CloudWatch en EC2.
## Instalacion del Agente.
- [Documentacion Oficial de AWS para la instalacion del Agente segun Sistema Operativo](https://docs.aws.amazon.com/es_es/AmazonCloudWatch/latest/monitoring/install-CloudWatch-Agent-on-EC2-Instance.html)
![image](https://github.com/user-attachments/assets/fc3cfe51-ca11-4531-aace-603298827ca1)

## Configuracion.
- Ejecutar dentro de la ruta /opt/aws/bin se encuentra el script amazon-cloudwatch-agent-config-wizard que es el Asistente de configuración del agente de CloudWatch.
![image](https://github.com/user-attachments/assets/c8f32327-62a2-434c-9565-174897af7dcf)

- Responder las preguntas para personalizar el archivo de configuración de su servidor.
- Finalizado, esto nos genera un archivo llamado config.json con todas las personalizaciones.
![image](https://github.com/user-attachments/assets/17a6ca89-33bb-4573-8a3b-ee7298e4aa1e)

## Crear un Rol.
- Vamos a crear un Rol con el tipo de Entidad **`AWS Service`**, **`EC2`**, **`CloudWatchAgentServerPoicy`**.
![image](https://github.com/user-attachments/assets/95e5adbe-1df9-4da5-a262-3462e4e44b17)

- Asignamos el Rol a la instancia donde se encuentra nuestro Agente (**`Actions`** - **`Security`**, **`Modify Iam Role`**).
![image](https://github.com/user-attachments/assets/20439027-270d-40da-811b-107f5ce486cd)

## Arrancar y Probar el Agente.
- Ejecutar:
```
sudo /opt/aws/amazon-cloudwatch-agent/bin/amazon-cloudwatch-agent-ctl -a fetch-config -m ec2 -s -c file:opt/aws/amazon-cloudwatch-agent/bin/config.json
```
> [!NOTE]
> Recordar mirar la documentacion para Arrancar el Agente. En este caso es para un EC2 que ejecuta Linux.

- Visualizamos nuestras metricas en **`Metrics`**, **`CWAgent`**
![image](https://github.com/user-attachments/assets/f4b10fc9-04dd-409a-b889-06dd1c45eb78)

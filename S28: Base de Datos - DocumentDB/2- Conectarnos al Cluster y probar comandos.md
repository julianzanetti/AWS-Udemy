# Conectarnos al Cluster y probar comandos.
![image](https://github.com/user-attachments/assets/d72c94a3-c0c4-435b-a0f6-5f2f106caf13)

## Descargar el ficherito .pem.
![image](https://github.com/user-attachments/assets/20079ae4-5f55-484a-88bf-c67e5c07ce70)

## Vamos a conectarnos a traves de mongo shell
- `Descargar Mongosh`: [Documentacion Oficial Instalacion de Mongo shell](https://www.mongodb.com/docs/mongodb-shell/install/)

![image](https://github.com/user-attachments/assets/f08ba70b-1f0e-4ccb-9f2b-15a674ed516d)

- `Conectarnos al cluster con mongosh`
```
mongosh cluster-documentdb-1x.cluster-cxcui0ooscg2.sa-east-1.docdb.amazonaws.com:27017 --tls --tlsCAFile global-bundle.pem --retryWrites=false --username root --password <Insertesucontraseña> 
```

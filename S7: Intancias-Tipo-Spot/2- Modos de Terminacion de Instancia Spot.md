# Distintos modos de terminacion de una instancia Spot.
### Vamos a la solicitud de un tipo de instancia Spot.
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/4f87ed8e-ca7e-4c9f-ad1b-13e39da564f3)

## Nos dirijimos a Capacidad de destino y seleccionamos lo siguiente.
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/3d9e44c8-e873-4f66-aa0f-e45d1e70b048)

## Elegimos que hacer cuando se interrumpe una instancia spot (Terminar/Hinbernar/Parar).
#### Recordar que una instancia Spot puede finalizar o bien porque Amazon necesita utilizar este tipo de instancia o porque supero el precio que nosotros marcamos como STOP.
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/88ad63fb-5602-4cf6-b482-f1f02588c474)
#### Si elegimos parar o hibernar no podemos arrancarla manualmente, tenemos que esperar a que Amazon lo haga.

## Elegimos si queremos o no Reequilibrio de capacidad.
#### Esto lo que hace es que cuando nuestra instancia se queda sin espacio, amazon automaticamente puede levantar otro hardware con mayor capacidad y sustituir la que se interrumpio.
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/df36ce1a-3b57-4ff1-a0f0-dbd018709562)

### Podemos elegir entre solo lanzar o lanzar y terminar.
![image](https://github.com/julianzanetti/AWS-Udemy/assets/134458575/2b1924f7-e99b-4679-a434-bdf09cbb0246)
#### Lanzar: Inicia la nueva instancia y espera a que vos elijas terminar la otra o que Amazon directamente la termine.
#### Terminar: Inicia la nueva instancia y elimina la que sustituye.

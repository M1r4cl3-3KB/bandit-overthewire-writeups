# Bandit Nivel 15 --> Nivel 16

## Objetivo 
Para el siguiente ejercicio nos indica que debemos enviar la contraseña del bandit15 por el puerto 30001 del localhost pero ahora utilizando SSL encriptación ya que esta cifrada. 

## Comandos usados 
ncat -ssl 
echo 

## Evidencia 
![Nivel 15](./Imagenes/bandit15.png)

## Explicaciòn
Para este nivel usaremos una herrmienta conocida ncat, ya que con uno de sus parametros nos permite enviar peticiones al puerto 30001 por el localhost por lo que usamos el siguiente comando:
echo "8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo" | ncat --ssl localhost 30001
Y a continuacion nos indica que es Correct! y nos da la contraseña para el siguiente nivel

## Contraseña para el siguiente nivel 
kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx

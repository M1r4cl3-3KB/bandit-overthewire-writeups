# Bandit Nivel 14 --> Nivel 15

## Objetivo 
El siguiente ejercicio nos indica que utilizando la contraseña del usuario bandit14 nos podemos leguear enviandolo al puerto 30000 del localhost.  

## Comandos usados 
echo
nc
localhost

## Evidencia 
![Nivel 14](./Imagenes/bandit14.png)

## Explicaciòn
Para completar este nivel es necesario conocer la herramienta netcat o nc, ya que por medio de esta podemos enviar peticiones o strings con echo " ", para que el puerte reciba e interprete caracteres y asi nos devuelva un outpud
Si ponemos el comando nc localhost 30000 nos indica que debemos enviar la contraseña correcta, por lo que asumimos que hay un servicio por detras que esta operando como nos indica que debemos pasar la contraseña del bandit14 hacemos lo siguiente
echo "MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS" | nc localhost 300000
A lo que a la respuesta de esta nos dice Correct ! y la contraseña para el siguiente nivel . 


## Contraseña para el siguiente nivel 
8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo


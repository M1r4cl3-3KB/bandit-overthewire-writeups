# Bandit Nivel 16 --> Nivel 17

## Objetivo 
Para el siguiente nivel nos indica que las credenciales para bandit17 pueden ser obtenidas mediante la proporcion de la contraseña del bandit16 en un puerto desde el rango de 31000 a 32000 y nos pide que veamos cual es el servicio que esta escuchando por ahi
Y que averiguemos cual de ellos habla SSL y cual no, Solamente hay un servicio que nos puede dar las credenciales. 

## Comandos usados 
nmap 
ncat --ssl 
echo

## Evidencia
![Nivel 16](./Imagenes/bandit16.png)

## Explicaciòn
Para este nivel en concreto podemos crear nuestro propio script para la obtencion de puertos abiertos pero por esta ocasion lo manejaremos con el comando usado en pestesting nmap que nos permite escanear puertos dentro de una maquina, donde nos reportara por atributus que 
le demos que servicio corre dentro de el, para eso usamos el comando: 
nmap --open -T5 -n -p31000-32000 127.0.0.1 
Donde: 
--open le indicamos que busque solamente por los puertos que estan abiertos 
-T5 le decimos que tiene que trabajar con un time 5 que es el mas rapido, para que no se demore tanto generalmente se usa en busquedas rapida pero hace mas ruido
-n para que nos haga resolucion DNS ya que aveces puede demorar demaciado a la hora de responder y es menos ruidoso
-p le indicamos el rango de puertos que queremos que nos filtre para ver cual de ellos estan abiertos o cerrados.
Verificamos que hay varios puertos abiertos pero al pasarle el comando : 
echo "kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx" | ncat --ssl localhost 31790
Verificamos que nos da una clave rsa private key por la que podemos usarla para el siguiente nivel
Hacemos el mismo paso del nivel del sshkey_private que nos dieron para conectarnos con ssh -i sshkey_private bandit17@localhost -p 2220 y entrariamos. 
Podemos revisar la contraseña de bandit17 por la ruta cat /etc/bandit_pass/bandit17   

## Contraseña del nivel 17 

EReVavePLFHtFlFsjn3hyzMlvSuSAcRD

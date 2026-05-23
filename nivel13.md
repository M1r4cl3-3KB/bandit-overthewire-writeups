# Bandit Nivel 13 --> Nivel 14

## Objetivo 
El siguiente ejercicio nos indica que la contraseña para el siguiente nivel el bandit14 esta dentro de /etc/bandit_pass/bandit14 y que solo puede ser leida por el usuario bandit14
Nos indica que para este nivel no averiguaremos el hash, si no que nos da como pista un archivo llamado sshkey.private que es la llave privada de ssh del usuario bandit14. Nos pide que 
averiguemos como nos podemos conectar con esta informaciòn. 

## Comandos usados 
ls 
cat 
touch
nano
chmod 600
ssh -i 

## Evidencia 
![Nivel 13](./Imagenes/bandit13.png)


## Explicaciòn
Como no podemos leer el archivo donde se guardan las contraseñas de los usuarios el /etc/bandit_pass/bandit14 verficiamos que el contenido del archivo de sshkey.private pertenece a la llave privada
por ssh por que lo que podemos usarla desde nuestra terminal, pasos a seguir : 
1- Copiar todo el contenido del archivo sskey.private 
2- Cerrar momentaneamente el ssh con exit para irnos a nuestra terminal 
3- Crear un archivo con touch llamado ssh_key en donde copiaremos todo el contenido que copiamos de la carpeta sskey.private del usuario bandit14
4- Para poder utilizar credenciales de ssh privadas es necesario que el archivo tenga permisos unicamente de usuario y que no pueda ser ejecutado por nadie mas ni por el propio usuario
5- Por lo que le cambiamos de permisos con chmod 600 ssh_key de esa manera si revisamos con ls -la claramente solo tiene permisos de usuario para read y write como debe de ser 
6- Por ultimo nos autenticamos con ssh con un comando especial al momento de utlizar el ssh_key : 
ssh -i ssh_key bandit14@bandit.labs.overthewire.org -p 2220
Y nos autenticara automaticamente como el usuario bandit14
Ahora dentro del usuario bandit14 podemos irnos leer la ruta "cat /etc/bandit_pass/bandit14" para ver la contraseña del usuario 

## Explicación 2
Para este caso en concreto tambien podemos usar el mismo archivo de bandit13 que nos proporciona al sskey_private para autenticarnos desde su terminal usando el siguiente comando :
ssh -i sshkey.private bandit14@localhost 
Al indicarle localhost indica que se autenticara a la misma maquina a la que pertenece el bandit13, ya que las clases privadas si tu se la envias a otra PC u otro usuario dentro de la red le das autorización 
para que se pueda conectar por SSH y de igual manera tendrias autenticación. 


## Contraseña para el nivel 14 
MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS 



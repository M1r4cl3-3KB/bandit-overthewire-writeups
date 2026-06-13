# Bandit Nivel 32 --> Nivel 33 (Ultimo Nivel)

## Objetivo 
El siguiente nivel y el ultimo nos dice que despues de todo esta cosa del git, es hora de otra forma de escapar. Buena suerte. 


## Comandos usados 

## Evidencia 
![Nivel 32](./Imagen/bandit32.png)

## Explicaciòn
Para empezar al conectarnos por ssh con el hash que nos dio el nivel anterior, vemos una terminal con un mensaje que dice lo siguiente : 

Si escribimos lo que sea el outpud siempre sera en mayusculas por lo que no se puede hacer cat o ls etc para poder movernos por la terminal. 

Vemos que al poner $HOME si nos muestra que es /home/badit32 Permission denied Por lo que si capta variables a nivel del sistema. 

Intentamos ver que shell usa y vemos que no podemos ver nada, pero dentro del conectexto de linux, existe un comando interno para poder ver que bash tienes o para llamar a una bash --> "echo $0"

por lo que dentro de esta terminal que parece interpretar comandos como python podemos pedirle una bash o el tipo de shell que esta usando con "$0" 

Por lo que nos dara una shell interactiva, si escribimos bash ahora nos dara una shell con la que podremos movernos libremente dentro de bnadit33.

Entramos dentro de la ruta de bandit33 --> cd /home/bandit33 y ejecutamos el comando --> "ls". Vemos un archivo llamado README.txt. 

Congratulations on solving the last level of this game!

At this moment, there are no more levels to play in this game. However, we are constantly working
on new levels and will most likely expand this game with more levels soon.
Keep an eye out for an announcement on our usual communication channels!
In the meantime, you could play some of our other wargames.

If you have an idea for an awesome new level, please let us know!

Para termiar leemos el archivo de /etc/bandit_pass/bandit33 y nos dara el ultimo hash de bandit33



## Contraseña para el siguiente nivel 

tQdtbs5D5i2vJwkO8mEyYEyTL8izoeJ0

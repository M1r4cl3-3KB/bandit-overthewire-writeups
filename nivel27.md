# Bandit Nivel 27 --> Nivel 28

## Objetivo 

El siguiente nivel nos dice que hay un repositorio ssh://bandit27-git@localhost/home/bandit27-git-repo, y que la contraseña para el usuario bandit27-git es la misma que usamos para autenticarnos a bandit27

## Comandos usados 
git 

## Evidencia 
![Nivel 27](./Imagen/bandit27.png)

## Explicaciòn
Para este nivel de igual manera nos genera un error si lo hacemos desde el bandit27 por lo que clonaremos el repositorio desde nuestra consola : 

Creamos un nuevo espacio de trabajo con permisos con mktemp -d y nos movemos a esa ruta con cd "ruta"

Clonamos --> git clone ssh://bandit27-git@bandit.labs.overthewire.org:2220/home/bandit27-git/repo 

Nos pedira poner la contraseña de bandit27 la cual es la siguiente "upsNCc7vzaRDx6oZC6GiR6ERwe1MowGB" 

Seguidamente se descargara un directorio llamado REPO accedemos a el y vemos que existe un archivo llamado README el cual contiene el siguiente texto : 

The password to the next level is: Yz9IpL0sBcCeuG7m9uQFt8ZNpS4HZRcN

## Contraseña para el siguiente nivel 

Yz9IpL0sBcCeuG7m9uQFt8ZNpS4HZRcN

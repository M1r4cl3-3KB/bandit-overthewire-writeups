# Bandit Nivel 29 --> Nivel 30

## Objetivo 
Para este nivel nos dice que hay un repositorio ssh://bandit29-git@bandit.labs.overthewire.org:2220/home/bandit29-git/repo 
En el que la contraseña para el usuarios bandit29-git es la misma para el usarios bandit29.

## Comandos usados 
git clone 
git log
git show
git branch -a 
git checkout 

## Evidencia 
![Nivel 29](./Imagen/bandit29.png)

## Explicaciòn
Al descargarnos el repositorio de la siguiente manera : 
git clone ssh://bandit29-git@bandit.labs.overthewire.org:2220/home/bandit29-git/repo

Entramos a la carpeta repo y al leer el README nos da informacion de credenciales y algunas notas para bandit30, pero en contraseña aparece "no passwords in production!"

Por lo que revisaremos el git log para ver los commits correspondientes --> si pide la herramienta less al usar git log puedes usar --> git --no-pager less

Vemos que al abrir los commits con el comando git show "hash", no nos muestra mucha informaciòn util. Viendo como funciona github en internet encontramos acerca de la ramas, que son bifurcaciones o rutas que toma un proyecto donde se queda guardada informaciòn.

Para ver ramas usamos "git branch -a" y vemos una importante que es /dev

Para poder entrar o cambiarnos a otra rama del codigo que existe usamos "git checkout "nombre" en este caso dev"

Nos sale un mensaje que indica Switched to a new branch deb --> hacemos un ls y vemos que contiene un archivo llamado README.md al leerlo con "cat README.md" nos encontramos con las credenciales de bandit30 y su contraseña corresponediente. 

1 │ # Bandit Notes
   2 │ Some notes for bandit30 of bandit.
   3 │ 
   4 │ ## credentials
   5 │ 
   6 │ - username: bandit30
   7 │ - password: qp30ex3VLz5MDG1n91YowTv4Q8l7CDZL


## Contraseña para el siguiente nivel 

qp30ex3VLz5MDG1n91YowTv4Q8l7CDZL

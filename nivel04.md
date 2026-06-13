# Bandit Nivel 4 --> Nivel 5

## Objetivo 
Para este nivel hay un archivo que se encuentra dentro del directorio "inhere" el cual solamente tiene permisos readable-human

## Comandos usados 
ls
cd inhere
find . -type f -readable | xargs file

## Evidencia
![Nivel 04](./Imagenes/bandit04.png)

## Explicacion

Al listar bandit3 con el comando "ls" encontramos un directororio llamado "inhere", al cual accedemos con el comando "cd inhere"
observamos que nos encontrarmos con distintos archivos llamados -file0X, como nos dice que solo hay 1 que es humanamente legible usamos
el comando find para encontrar . todo lo que hay dentro -type f que sea de tipo file osea archivo -readable que sea legible(que se pueda leer)
y concatenamos con una pipeta con el comando xargs que nos permite ejecutar otro comando pararelo al output del primer comando seguido de file 
que nos permite listar que tipo de archivo es si es data o si es ASCII text, observamos que el archivo llamado ./-file07 es el unico que tiene 
estas caracteristicas por lo que al hacerle un cat nos muestra la contraseña para el siguiente nivel 

## Contraseña para el siguiente nivel 

4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw

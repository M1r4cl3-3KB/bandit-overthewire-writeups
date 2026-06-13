# Bandit Nivel 2 --> Nivel 3

## Objetivo 
Para este nivel tenemos un directorio llamado inhere el cual contiene un archivo oculto que no se visualiza con 
el comando ls normal llamado ...Hidding-From-You dentro de bandit3

## Comandos usados 
ls
ls -l 
cd inhere
cat /home/bandit3/inhere/...Hidding-From-You

## Evidencia
![Nivel 03](./Imagenes/bandit03.png)

## Explicaciòn 

Utilizamos el comando ls para listar los archivos o directorios dentro de la carpeta de bandit3 lo que nos muetra un
carpeta llamada inhere, Utilizamos el comando cd para poder movernos a la carpeta "change directoroy" de la siguiente manera
"cd inhere", a continuacion verificamos que al hacer ls no nos lista nada, como indica el ejercicio hay un archivo oculto, para 
esto hacemos uso del comando ls -l para listar todo lo que hay dentro y vemos un archivo llamado Hidding-For-You, para leerlo usamos
de la misma forma absoluta con cat para leerlo, "cat /home/bandit3/inhere/...Hiddin-From-You 

## Contraseña para el siguiente nivel 

2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ

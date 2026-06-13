# Bandit Nivel 8 --> Nivel 9

## Objetivo
Este ejercicio nos da un archivo data.txt en el cual debemos encontrar la unica linea de texto que se repite solamente una vez en el archivo

## Comandos usados
cat 
grep 
uniq -u 
sort 

## Evidencia
![Nivel 08](./Imagenes/bandit08.png)


##Explicaciòn
Si leemos el archivo nos muestra que hay 1001 lineas disponibles por lo que verificar al ojo o manualmente nos tomara mucho tiempo, usamos de expresiones
que nos permiten filtrar datos en un archivo de esa manera al combinar y utilizar el siguiente comando nos dara la unica linea que no se repite mas de 2 veces
cat data.txt | sort | uniq -u --> sort ordena de arriba hacia abajo de manera que pone juntas todas las lineas que se repiten y al usar 
		                  uniq -q  elimina todas las lineas que se repitan dejando asi solo las unicas lineas que no se repitan dejandonos con la contraseña 
para el siguiente nivel. 

## Contraseña para el siguiente nivel
4CKMh1JI91bUIZZPXDqGanal4xvAg0JM

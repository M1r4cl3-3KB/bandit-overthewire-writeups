# Bandit Nivel 10 --> Nivel 11

## Objetivo
El siguiente ejercicio nos indica que dentro de un archivo llamado data.txt contiene data que esta codificada con base64 por lo que debemos revertir esa codificacion

## Comandos usados
ls 
cat
base64 -d 

## Evidencia
![Nivel 10](./Imagenes/bandit10.png)


##Explicaciòn
Lo que debemos de hacer primeramente es leer el archivo data.txt para ver el mensaje en base64, debemos copiar todo el texgo que nos muestra y seguidamente utilizar el siguiente comando
echo 'VGhlIHBhc3N3b3JkIGlzIGR0UjE3M2ZaS2IwUlJzREZTR3NnMlJXbnBOVmozcVJyCg==' | base64 -d 
Este comando nos permite imprimir con echo el texto pero de forma paralela desencodearlo con base64 -d de decode de esa manera nos muestra el codigo normal antes de que fuera encodeado 
The password is dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr

 
## Contraseña para el siguiente nivel
dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr

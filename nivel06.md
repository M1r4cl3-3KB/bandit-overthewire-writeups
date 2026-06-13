# Bandit Nivel 6 --> Nivel 7

## Objetivo
El objetivo de este nivel es encontrar un archivo que esta en el servidor y tiene las siguientes propiedades:
- El archivo le pertenece al usuario bandi7
- El archivo le pertenece al grupo bandit 6
- El archivo tiene en peso de 33 byes

## Comandos usados
cat
find
-type f -user bandit7 -group bandit6 -size 33c
2>/dev/null

## Evidencia
![Nivel 06](./Imagenes/bandit06.png)


##Explicaciòn
Como nos pide encontrar el archivo en todo el sistema utilizamos directamente el comando find / que busca desde la raiz 
a diferencia del . (punto) que solo buscaba en el directorio actual en el que te encuentras, seguidamente podemos filtrar por
el nombre del usauario y grupo del archivo, tambien filtramos por el tamaño del archivo dejando asi un comando como el siguiente :
find / -type f -user bandit7 -group bandit6 -size 33c 2>/dev/null --> Redirigimos el STDER al vacio, como lo ejecutamos como el usuario 
bandit6 actualmente si no ponemos esto ultimo nos filtrara archivos de los que no tengamos permiso acceder u otra indole por que si es necesario
ponerlo para que nos filtre solo las respuestas positivas o correctas dejandonos la siguiente ruta absoluta : /var/lib/dpkg/info/bandit7.password
Utilzando cat para leer archivo nos deja con la contraseña para el siguiente nivel. 

## Contraseña para el siguiente nivel
morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj

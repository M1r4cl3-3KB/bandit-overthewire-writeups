# Bandit Nivel 11 --> Nivel 12

## Objetivo
El siguiente nivel nos indica que hay un archivo llamado data.txt donde todas las letras desde la (a-z) y (A-Z) han sido rotadas 13 posiciones hacia adelante.
Para poder obtener la contraseña debemos rotar 13 posiciones antes para que sea legible el archivo. 


## Comandos usados
cat 
echo
tr 'a-zA-Z' 'n-za-mN-ZA-M'

##Explicaciòn
Dentro del archivo data.txt encontramos un string que esta rotado 13 posiciones por lo que si la letra empieza con G antes era T como son 13 posiciones podemos 
usar el comando tr que transforma un segmento de letras a otras permitiendo asi utilizar el abecederio que conocemos normalmente de la A hasta la Z para poder moder
todo lo que sea A sera N, y que vaya rotando por ejemplo si hubiera luego una B ahora seria O para entederlo mejor dejaremos la siguiente lista para entenderlo
A B C D E F G H I J K L M N O P Q R S T U V W X Y Z 
N O P Q R S T U V W X Y Z A B C D E F G H I J K L M
De esta manera tr interpretara que todo se debe mover 13 posiciones por lo que al final nos sale el siguiente mensaje: 
Gur cnffjbeq vf 7k16JArUVv5LxVuJfsSVdbbtaHGlw9D4 --> String del archivo
The password is 7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4 --> String modificado con tr


## Contraseña para el siguiente nivel
7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4
